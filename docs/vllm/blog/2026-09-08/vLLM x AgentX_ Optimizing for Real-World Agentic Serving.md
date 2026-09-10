# vLLM x AgentX 優化重點摘要

- **來源**: vllm.ai
- **發布日期**: 2026-09-08
- **原文連結**: https://vllm.ai/blog/2026-09-08-vllm-agentx

## 核心主題
vLLM 針對代理工作負載優化三大策略，透過混合 KV 快取管理與執行平面優化，顯著提升代理服務效率與成本效益。

## 關鍵重點
- **性能表現**：DeepSeek V4 Pro 達 130K tokens/GPU-second，MiniMax M3 達 376 tokens/秒互動性，Kimi K3 達 62.7 tok/s
- **成本優勢**：相比 Opus 5 API 有 14.6x–106x 的 serving-cost 優勢
- **優化策略**：混合 KV 快取管理、分層 KV 快取卸載、前綴快取保留
- **執行效率優化**：Kimi K3 採用 DCP 降低解碼延遲，DeepSeek V4 採用 PCP 提升預填充速度
- **解決 Head-of-Line Blocking**：使用 --long-prefill-token-threshold 限制長預填充 token 數，TPGS 提升達 93%
- **P/D 比率動態平衡**：根據並發量與上下文長度調整，最大化吞吐量

## 結論
vLLM 透過混合 KV 快取管理與執行平面優化，成功解決代理服務中的長上下文與多輪會話挑戰，同時大幅降低服務成本，為實際代理部署提供可參考的優化方案。

---

## 失敗經驗與未來方向
- Pipeline Parallelism 不適合溫暖代理轉（prefill 太短）
- DCP 對 DeepSeek V4 效果不如 DEP
- Load balance 不如 Session-aware sticky routing（因 KV cache 局部性）
- 未來方向：明確代理結構、支援 Agent hints、可編程 KV cache 管理、Session-based KV cache 管理
