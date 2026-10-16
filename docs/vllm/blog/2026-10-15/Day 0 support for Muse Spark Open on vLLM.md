# Day 0 support for Muse Spark Open on vLLM

- **來源**: vLLM Blog
- **發布日期**: 2026-10-15
- **原文連結**: https://vllm.ai/blog/2026-10-15-muse-spark-open

## 核心主題
vLLM 正式支援 Meta 的 Muse Spark Open 開源模型，提供 Day 0 部署支援，支援多架構硬體。

## 關鍵重點
- 模型架構：816B 總參數，42B 活躍參數，1M 上下文窗口，支援圖片、影片和音頻的多模態感知
- 硬體支援：Nvidia、AMD 和 TPU 平台，支援 Tensor Parallelism 和 Pipeline Parallelism
- 量化格式：Meta 提供 BF16 和 NVFP4 兩種量化版本，AMD 額外提供 MXFP4
- DSpark 推測解碼加速：使用 DSpark 草稿模型提升推理速度，支援 CUDA 和 ROCm
- 推理優化：Nvidia 和 AMD 團隊分別針對各自硬體進行了 FlashInfer 和 vLLM 的優化

## 結論
vLLM 與 Meta 合作，為開發者提供即開即用部署方案，並透過 DSpark 加速和硬體優化提升性能，是當前最強大的 US 開源權重模型。
---
