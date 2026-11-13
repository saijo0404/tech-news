# Inkling 2 Small on vLLM: Day-0 Support

- **來源**: vLLM Blog
- **發布日期**: 2026-11-12
- **原文連結**: https://vllm.ai/blog/2026-11-12-inkling2-small

## 核心主題
vLLM 正式支援 Thinking Machines 的 Inkling 2 Small 多模態混合專家模型，提供 Day-0 級別的原生優化支援，包括 DSpark 猜測器與高效能推論。

## 關鍵重點
- **模型規格**: 總參數 594B，活躍參數 17B，支援 1M tokens 上下文，48 層 MoE 架構搭配 384 專家（Top-8 選取）
- **架構升級**: 相比 Inkling 引入 Block Attention Residuals、Gated Attention、Attention Sink 以及 23 層 ViT 影像編碼器
- **混合精度 MoE**: 前 40 層使用 NVFP4，後 8 層使用 MXFP8，可單節點部署
- **原生 DSpark 猜測器**: 搭配 RNN 頭部，每步驟推斷 7 個 token，提升推論速度
- **vLLM 優化**: 透過 Kernel Fusion、PDL、Sequence Parallelism 及優化 Gluon 注意力核，TP4 時達 630 tok/s/用戶
- **RL 與 LoRA 支援**: 支援 SkyRL 演算法及 LoRA 精細化訓練

## 結論
vLLM 成功整合 Inkling 2 Small 並提供 Day-0 級別優化，使該多模態模型能在 GB200 硬體上高效推論，同時保持與參考實作一致的準確性，為未來多模態應用奠定基礎。
---
