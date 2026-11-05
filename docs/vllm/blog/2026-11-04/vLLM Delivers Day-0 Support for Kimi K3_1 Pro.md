# vLLM Delivers Day-0 Support for Kimi K3.1 Pro

- **來源**: vllm.ai
- **發布日期**: 2026-11-04
- **原文連結**: https://vllm.ai/blog/2026-11-04-kimi-k31-pro

## 核心主題
vLLM 首日即支援 Moonshot AI 的 Kimi K3.1 Pro 模型，透過稀疏注意力機制與混合 KV Cache 架構，在 NVIDIA GPU、AMD GPU、Google TPU 及 Alibaba T-Head Zhenwu PPU 上實現高效能推理。

## 關鍵重點
- **稀疏注意力 (DSA) 全面支援**：Kimi K3.1 Pro 所有 24 全注意力層加入 DSA 索引器，長上下文解碼時每層記憶體讀取減少 77%，8× GB300 可同時處理 36 個完整 1M token 上下文。
- **混合 KV Cache 架構**：整合 MLA 潛在、索引鍵與 KDA 狀態，支援 FP8/NVFP4 潛在與 MXFP4 索引鍵，8× GB300 可處理 1.7 倍更多 token。
- **顯著性能提升**：Token-sharded Prefill 在 340K tokens 下快 1.69 倍，DCP Prefill 快 4.1-4.3 倍，DCP8 解碼速度提升 1.2-1.6 倍，DSpark 猜測解碼快 3.0 倍。
- **硬體優化與零不匹配 RL**：NVIDIA Rubin 單用戶最高 815.6 tok/s，AMD MI355X 原生 MXFP4 索引器減少 48.5% 索引緩存，vLLM 與 Megatron 產生完全一致的 log-probs。

## 結論
vLLM 透過首日即支援 Kimi K3.1 Pro 的稀疏注意力與混合 KV Cache 架構，大幅降低長上下文推理成本並提升吞吐量，同時提供零不匹配 RL 訓練能力，為大模型推理服務帶來重大突破。

---