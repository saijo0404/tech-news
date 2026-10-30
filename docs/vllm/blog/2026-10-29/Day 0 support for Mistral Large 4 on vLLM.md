# Day 0 support for Mistral Large 4 on vLLM

- **來源**: vLLM
- **發布日期**: 2026-10-29
- **原文連結**: https://vllm.ai/blog/2026-10-29-mistral-large-4

## 核心主題
vLLM 正式支援 Mistral Large 4 模型，提供 Day 0 支援並包含多種性能優化技術，包括 DSpark 推測解碼、長上下文處理及 AMD GPU 支援。

## 關鍵重點
- **模型架構**：72 層 MoE 架構，128 個專家（top-4 路由），總參數 1 兆，每 token 活躍參數 490 億，支援多模態（Pixtral 視覺編碼器）
- **性能優化**：DSpark 推測解碼吞吐量提升 1.9–2.2 倍，長上下文 DCP 提升 7.9 倍，TTFT 提升 1.6 倍
- **AMD 支援**：Day 0 即支援 AMD Instinct MI350 系列 GPU，支援 TP4/TP8 部署
- **記憶體優化**：NVFP4 量化記憶體佔用少 1.5 倍，解碼速度快 1.08–1.22 倍，GSM8K-200 準確率達 0.965-0.980
- **部署方式**：提供 Docker 映像 vllm/vllm-openai:mistral-large-4，支援 DSpark 推測解碼與長上下文處理

## 結論
vLLM 成功實現 Mistral Large 4 的 Day 0 支援，透過 DSpark 推測解碼、長上下文處理及 AMD GPU 優化，大幅提升推理性能與記憶體效率，為多模態大模型部署提供完整解決方案。

---
