# 使用 JAX 與 MaxText 搭配 NVIDIA Blackwell 上的 NVFP4 加速模型訓練

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-08
- **原文連結**: https://developer.nvidia.com/blog/train-models-faster-with-jax-and-maxtext-using-nvfp4-on-nvidia-blackwell/

## 核心主題
本文介紹 NVIDIA Transformer Engine 中的 NVFP4 混合精度訓練配方，搭配 JAX 與 MaxText 框架在 NVIDIA Blackwell 架構上實現高效能的 4-bit 模型預訓練，在無顯著精度損失的前提下帶來高達 1.73 倍的加速。

## 關鍵重點
- **NVFP4 格式的五大技術要點**：採用 16 元素微區塊縮放、E4M3 尾數比例因子、隨機哈達瑪變換（僅用於權重梯度 GEMM）、2D 權重縮放，以及隨機取整，這些技術共同確保 4-bit 精度下的模型收斂品質，相比 MXFP4 可減少約 36% 的訓練 token 需求。
- **MaxText 中的 NVFP4 實作方式**：僅對 Transformer 的 MLP（前饋）層應用 NVFP4 量化，注意力區塊則保持較高精度以避免 softmax 放大量化雜訊；提供兩種模式（含/不含隨機哈達瑪變換），透過單一 `quantization` 旗標即可切換。
- **實測效能提升顯著**：在 GB200 與 GB300 超級晶片上，Llama 3 8B 與 Llama 3.1 405B 模型的 NVFP4 配方相較 FP8 基線帶來 1.31x 至 1.73x 的加速（GPU 每卡可提升 500-700 TFLOP/s），同時 Llama 3 8B 的訓練損失曲線與 FP8 幾乎完全重疊，確認無可測量的精度損失。

## 結論
NVFP4 配方透過在 JAX/MaxText 中整合低精度訓練技術，讓開發者能在 NVIDIA Blackwell 架構上以極低的精度開銷獲得顯著的速度提升，為大規模 LLM 預訓練提供了一個兼具效能與精度的實用方案。
