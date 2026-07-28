# Kimi K3 Is Here: Efficient Day-0 Support on vLLM

- **來源**: vLLM
- **發布日期**: 2026-07-27
- **原文連結**: https://vllm.ai/blog/2026-07-27-k3

## 核心主題
vLLM 正式支援 Kimi K3 模型，提供高效能的 Day-0 部署解決方案，整合 DSpark 推測解碼、混合前綴緩存等關鍵優化技術。

## 關鍵重點
- **模型規格**：2.8 兆參數 Mixture-of-Experts 模型（16 of 896 experts 每 token 激活），支援 1M token context window 與 native vision
- **性能表現**：無推測解碼時 118 tok/s，使用 DSpark 推測解碼可達 370 tok/s（3.14 倍提升）
- **硬體需求**：8 NVIDIA B300 或 8 AMD MI355X GPUs（最小配置），推薦 GB300 NVL72 集群部署
- **主要技術特性**：支援 DSpark 推測解碼、prefill/decode 解耦、agentic KV caching、工具調用與結構化輸出
- **緩存優化**：混合 KDA 與 full-attention 的前綴緩存策略，支援 Interval-based 與 Marconi-style 兩種保留策略
- **AMD 支援**：vLLM 正式支援 Kimi K3 在 AMD GPU 上運行，隨版本發布即支援 ROCm

## 結論
vLLM 成功實現了 Kimi K3 模型的生產級部署，提供完整的 Docker 部署方案、效能數據與最佳實踐指南，為開發者帶來即開即用的高效能解決方案。
---
