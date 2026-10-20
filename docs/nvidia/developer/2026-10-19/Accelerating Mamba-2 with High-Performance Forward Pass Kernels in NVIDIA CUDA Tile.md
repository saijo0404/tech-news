# Accelerating Mamba-2 with High-Performance Forward Pass Kernels in NVIDIA CUDA Tile

- **來源**: developer.nvidia.com/blog
- **發布日期**: 2026-10-19
- **原文連結**: https://developer.nvidia.com/blog/accelerating-mamba-2-with-high-performance-forward-pass-kernels-in-nvidia-cuda-tile/

## 核心主題
文章介紹了如何使用 NVIDIA CUDA Tile (cuTile) 實現 Mamba-2 狀態空間模型的前向通過優化，並展示了比 Triton 實現快 1.14x 至 1.82x 的性能提升。

## 關鍵重點
- **cuTile 架構優勢**：cuTile 是 Python 基的並行編程模型，可自動利用 Tensor Cores 等 GPU 硬體特性，將 Mamba-2 前向傳播的三個計算階段整合為單一 tiled kernel。
- **三個核心核優化**：
  - **chunk_cumsum**：計算每 token、每 head 的衰減項累積和（對數空間），使用 cuTile 的 ct.cumsum 原語
  - **fwd_pass_state**：使用 ct.mma 執行 Tensor Core 矩陣乘法，推進隱藏狀態，應用跳躍公式與指數衰減
  - **compute_out**：融合狀態項、衰減與因果掩蔽互動矩陣、跳連接到單一瓦片核，中間矩陣保留在寄存器中並轉換為 TF32
- **關鍵優化技術**：
  - **Latency hint**：標註 DRAM 流量以優化編譯器排程
  - **Swap A/B**：利用 NVIDIA Blackwell Tensor Core 特性，將融合運算結果路由至 Operand A，減少共享記憶體競爭
  - **GMEM layout**：將 decay_cumsum 和 dt 轉置為 [batch, head, token] 佈局，啟用 TMA 提升記憶體存取效率
  - **Autotuner**：整合 cuTile 參數進行自動搜尋，針對不同輸入形狀自動尋找最佳化設定
- **性能表現**：比 Triton 實現快 1.14x 至 1.82x，序列長度與 state size 增加時，加速比進一步提升。測試硬體：NVIDIA B300 SXM6 (Blackwell Ultra)，1100W 功耗限制。
- **實現細節**：使用 cuTile 的 register 儲存 intermediate 結果，避免完整互動矩陣 C @ B.T 在 global memory 中 materialize，採用 ct.exp2 處理不穩定指數運算，即時 mask 避免 overflow。

## 結論
文章展示了 cuTile 在 Mamba-2 前向傳播實現上的優異性能，為大語言模型推理提供了新的加速方案。後續將介紹 cuTile 的 backward pass 實現。

---

測試環境：mamba_ssm 2.3.2.post1、Triton 3.7.1、cuTile 1.5.0、PyTorch 2.13.0、CUDA 13.3
