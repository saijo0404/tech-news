---
# Train Models Faster with JAX and MaxText Using NVFP4 on NVIDIA Blackwell

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-08
- **原文連結**: https://developer.nvidia.com/blog/train-models-faster-with-jax-and-maxtext-using-nvfp4-on-nvidia-blackwell/

## 核心主題
NVIDIA 推出 NVFP4 訓練配方，讓開發者能透過 JAX 與 MaxText 在 NVIDIA Blackwell 平台上進行高吞吐量、4-bit 混合精度大語言模型預訓練，在幾乎沒有準確度損失的情況下，相較於 FP8 取得 1.31 至 1.73 倍的加速。

## 關鍵重點
- **NVFP4 格式的五項關鍵技術**：採用 16 元素微區塊縮放（小於 MXFP4 的 32 元素）、E4M3 區塊縮放因子搭配每張量 FP32 縮放、僅對 WGRAD GEMM 輸入套用隨機哈達瑪變換、2D 權重縮放（16×16 區塊一個 FP8 縮放）以及隨機取整，共同確保 4-bit 精度下的收斂品質。
- **精確的量化策略**：NVFP4 僅對 Transformer 的 MLP（前饋）層三個 GEMM 套用 NVFP4 量化，注意力區塊維持較高精度，因為 softmax 會指數級放大量化雜訊；MLP 佔大多數訓練 FLOPs，此策略捕捉了大部分加速同時避免收斂風險。
- **顯著的效能提升與零準確度損失**：在 Llama 3 8B 模型上，GB200 實現 1.35 倍加速、GB300 實現 1.31 倍加速；Llama 3.1 405B 在 GB200 實現 1.44 倍加速、GB300 實現 1.73 倍加速；10,000 步預訓練顯示 NVFP4 與 FP8 基準的損失曲線幾乎完全重疊（收斂期平均差距僅 +0.026 nats）。

## 結論
NVFP4 配方讓 AI 工廠能在相同時間預算內訓練更多更大的模型，或以更短時間完成訓練。開發者可從 NVIDIA JAX-Toolbox 獲取 MaxText NVFP4 訓練腳本，在 Blackwell 平台上輕鬆啟用，享受更高運算吞吐量同時不犧牲模型品質。

---
