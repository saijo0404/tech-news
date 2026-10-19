# Scaling Kimi K3 on AMD Instinct MI355X

- **來源**: vllm.ai
- **發布日期**: 2026-10-16
- **原文連結**: https://vllm.ai/blog/2026-10-16-kimi-k3-mi355x

## 核心主題
Kimi K3 模型在 AMD Instinct MI355X 上實現了比 NVIDIA HGX B300 更高的每 GPU 效能，通過六項關鍵優化技術達成。

## 關鍵重點
- AgentX 架構在 AMD MI355X 上運行 Kimi K3，比 NVIDIA HGX B300 每 GPU 每秒多處理 24.4% 的 token
- 在成本模型下，每美元可獲得 87.4% 更多的 token
- 六大優化技術包括 Cache 優化、MoE 優化、記憶體流量優化、MLA 優化、KDA 優化和推測解碼優化
- KDA 在 4K 和 16K 輸入長度上比 Triton 多提供 5.3–5.6% 的輸入吞吐量
- AMD Instinct MI355X 比 NVIDIA HGX B300 每 token 成本低 46.6%

## 結論
AMD Instinct MI355X 通過 KDA 和 AgentX 架構的優化，在 Kimi K3 模型上實現了比 NVIDIA HGX B300 更高的效能和成本效益，特別適合需要高吞吐量和低成本的場景。
---