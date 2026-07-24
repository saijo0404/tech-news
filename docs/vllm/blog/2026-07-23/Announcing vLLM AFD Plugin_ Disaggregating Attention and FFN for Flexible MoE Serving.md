# Announcing vLLM AFD Plugin: Disaggregating Attention and FFN for Flexible MoE Serving

- **來源**: vLLM Blog
- **發布日期**: 2026-07-23
- **原文連結**: https://vllm.ai/blog/2026-07-23-vllm-afd-plugin

## 核心主題
vLLM 推出 AFD Plugin，將混合專家（MoE）模型的 Attention 與 FFN 層解耦為獨立服務，實現更靈活的推理架構。

## 關鍵重點
- **獨立擴展能力**：Attention 與 FFN 可各自獨立擴展，解決不同工作負載的擴展需求差異
- **硬體支援**：支援 NVIDIA GPU 與 Ascend NPU，提供同步與異步兩種連接方式
- **模型支援**：支援 DeepSeek V2/V3 系列模型及 GLM MoE DSA 架構
- **性能優化**：同步模式在 Decode 階段提升吞吐量，異步模式在 Prefill 階段降低首字延遲
- **實驗性質**：目前仍為實驗性專案，需更多大規模測試驗證

## 結論
vLLM AFD Plugin 透過解耦 Attention 與 FFN 架構，為 MoE 模型服務提供更大彈性，但作為實驗性專案仍需更多實測驗證。

---