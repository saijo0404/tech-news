# vLLM Support for NVIDIA Vera Rubin NVL72: 7.8x Throughput over GB200 NVL72

- **來源**: vLLM Blog
- **發布日期**: 2026-10-09
- **原文連結**: https://vllm.ai/blog/2026-10-09-vera-rubin-preview

## 核心主題
vLLM 正式支援 NVIDIA Vera Rubin NVL72 硬體，在 AgentX 測試中實現比 GB200 高 7.8 倍的吞吐量，並提供 Day-0 即開即用支援。

## 關鍵重點
- **硬體性能提升**：Vera Rubin NVL72 提供 5 倍 NVFP4 FLOPS、2.4 倍 HBM 頻寬和 1.7 倍 NVLink 頻寬，且 softmax 指數運算速度提升 2-4 倍
- **Day-0 即開即用**：基於 Blackwell 架構，vLLM 無需修改即可運行，支援 DeepSeek、Kimi、GLM 和 MiniMax 等多種模型
- **本地域支援**：利用 CUDA 13.4 的本地域功能優化 MoE 解碼，小 token 前向傳遞可獲得 1.2 倍加速
- **性能突破**：AgentX 測試中實現 7.84 倍吞吐量提升，MLPerf VLM 測試中實現 3.7 倍吞吐量提升

## 結論
這是 vLLM 在 Vera Rubin 平台上的早期成果，隨著更多優化持續進行，預期會看到更多性能提升。
---
