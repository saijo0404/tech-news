# 以 JAX 和 MaxText 搭配 NVIDIA Blackwell 的 NVFP4 加速模型訓練

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-08
- **原文連結**: https://developer.nvidia.com/blog/train-models-faster-with-jax-and-maxtext-using-nvfp4-on-nvidia-blackwell/

## 核心主題
NVIDIA 發布 NVFP4 訓練配方，結合 Transformer Engine 與 MaxText 在 JAX 中實現 4 位元混合精度預訓練——在 NVIDIA Blackwell（GB200/GB300）上帶來 1.31 至 1.73 倍的吞吐量加速，且相較 FP8 基線無顯著精度損失。

## 關鍵重點
- **NVFP4 格式五大關鍵技術：16 元素微區塊縮放、E4M3 指數、Random Hadamard Transform、2D 權重縮放與隨機捨入**：NVFP4 配方以五項技術共同維持收斂——（1）微區塊縮放使用 16 元素區塊（為 MXFP4 32 元素區塊的一半），使單一異常值對共享縮放的影響降低；（2）E4M3 區塊縮放因子使用尾數位（mantissa bits）而非 MXFP4 的 E8M0 冪次縮放，並疊加張量層級 FP32 縮放，在 8B 參數、1T token 實驗中，MXFP4 需約 36% 更多 token 才能匹配 NVFP4 最終損失；（3）Random Hadamard Transform 僅套用於 WGRAD GEMM 輸入以高斯化異常值，跳過 FPROP 與 DGRAD 以避免打破 2D 縮放一致性；（4）2D 權重縮放使用每 16×16 權重區塊一個 FP8 縮放，使 FPROP 與轉置 DGRAD 使用相同縮放；（5）隨機捨入（Stochastic Rounding）以無偏方式防止微小更新被壓成零。NVFP4 僅套用於 Transformer 的 MLP（前饋）層 GEMM，注意力區塊保持較高精度，因為 softmax 會指數性放大 QK^T 分數的量化雜訊。
- **GB200 與 GB300 實測性能：1.31× 至 1.73× 吞吐量加速，405B 大模型增益最大**：以 Llama 3 8B 與 Llama 3.1 405B 在 GB200 與 GB300 上的 NVFP4 對比 FP8 基準——Llama 3 8B 在 GB200 上從 1,497 增至 2,017 TFLOP/s（1.35×）、GB300 從 1,759 增至 2,301 TFLOP/s（1.31×）；Llama 3.1 405B 在 GB200 上從 1,557 增至 2,241 TFLOP/s（1.44×）、GB300 從 2,103 增至 3,633 TFLOP/s（1.73×）；每 GPU 持續吞吐量在每個配置上增加 500-700 TF/s；最大相對增益出現在 405B 配置（GB200 1.44×、GB300 1.73×），因為步驟級 GEMM 質量主導 FSDP 集體開銷，精度層級的加速直接轉化為壁鐘節省。
- **精度驗證：10,000 步訓練損失曲線完全重疊，無可測量精度損失**：以 C4 資料集進行 Llama 3 8B 預訓練 10,000 步，FP8 基線與 NVFP4 的損失曲線完全重疊——兩者從約 12.2 nats 下降至約 3.9 nats，收斂 regimes 的平均差距僅 +0.026 nats，遠小於步驟間雜訊；MaxText NVFP4 配方提供兩種模式：`quantization=te_nvfp4`（含 Random Hadamard Transform，推薦於收斂不佳時使用）與 `quantization=te_nvfp4_no_rht`（無 RHT、最低開銷，但可能降低收斂品質）；透過設定 `quantization=te_fp8_delayedscaling` 可產生 FP8 基線進行比較。

## 結論
NVFP4 配方為大型語言模型預訓練開啟了 4 位元精度的實用路徑——在 NVIDIA Blackwell 硬體上，透過精心設計的五大技術組合，NVFP4 不僅在吞吐量上超越 FP8 高達 73%，更在 10,000 步訓練中證明無可测量的精度損失；對於以吞吐量為命的 frontier LLM 訓練而言，每一秒的步驟時間縮短都能累積為數天的訓練與大量運算成本節省；NVFP4 僅聚焦 MLP 層的量化以避開注意力 softmax 的量化雜訊放大風險，同時保持 2D 縮放一致性確保 FPROP 與 DGRAD 的轉置對稱性——這種「精準打擊」策略讓低比特預訓練從理論走向工程實踐；開發者可透過 MaxText 容器與 `nvfp4_example.sh` 腳本立即在 Blackwell 上嘗試 NVFP4 訓練，而 NVIDIA 也持續展望 Rubin 平台的 NVFP4 吞吐量潛力。
