# vLLM × HPC-Ops: High-Performance Attention and MoE Backends from Tencent Hunyuan

- **來源**: vLLM Blog
- **發布日期**: 2026-07-06
- **原文連結**: https://vllm.ai/blog/2026-07-06-vllm-hpc-ops

## 核心主題
Tencent Hunyuan AI Infra 團隊開發的 HPC-Ops 生產級算子庫中的注意力與 MoE 核核已成為 vLLM 的一級後端，針對 NVIDIA Hopper 架構（特別是 H20）進行了優化。

## 關鍵重點
- **注意力後端**：採用每步驟動態負載平衡解碼調度器，在混合長度解碼中比靜態分割 KV 調度快達 2.95 倍，平均比 FlashInfer 和 FlashAttention 快 2.25 倍。
- **MoE 後端**：完全融合的低延遲 FP8 MoE 管道，在 TP8/EP1 下平均快 1.59 倍，TP1/EP8 下快 1.21 倍，優於 Triton 和 CUTLASS。
- **端到端性能**：在 8× H20 上運行 Hy3 模型時，TTFT 降低約 24%，TPOT 降低約 17%，最大批次大小下可達 30%。

## 結論
這些後端無需修改代碼即可通過 vLLM 標準後端介面整合，為生產環境中的 LLM 服務帶來顯著的性能提升，特別適合處理混合長度批次和 MoE 模型。

---
