# Taking vLLM Apart: A Practical Guide to Disaggregated Serving

- **來源**: vLLM
- **發布日期**: 2026-09-29
- **原文連結**: https://vllm.ai/blog/2026-09-29-disaggregated-serving-guide

## 核心主題
這篇文章介紹了 vLLM 分散式服務架構（Disaggregated Serving）的重點，將傳統單一進程同時處理的 prefill、decode 和 CPU 工作分開，以提升效能和降低延遲。

## 關鍵重點
- **四層架構設計**：將推理拆分為 render → prefill → decode → derender 四層，Render 層不佔用 GPU，可獨立擴展以處理高併發解析模型
- **主要優勢**：改善 goodput（可持續請求率）、降低尾延遲（ITL p99 從 169ms 降至 52ms）、獨立調配各階段並發數、長提示高併發場景效能提升 2.4 倍
- **關鍵技術**：使用 NIXL 作為 KV connector 負責 Prefill 與 Decode 之間的 KV Cache 傳輸，支援 Qwen3 等推理模型的解析（reasoning/tool-calling）
- **實作要點**：需 vLLM v0.30.0 以上，配置 VLLM_NIXL_SIDE_CHANNEL_PORT 唯一，可透過 return_token_ids 避免重複 tokenization
- **性能挑戰**：串流解析模型 CPU 消耗約為本地推理的 9 倍，長提示詞（100k token）佔請求體積 99%，傳輸效率低，解析狀態無法序列化

## 結論
分散式服務架構透過將推理階段分離，能有效提升長提示高併發場景的效能，但需要快速的 KV 傳輸（如 RDMA）和正確的部署配置。建議在 ITL p99 錯過 SLO、長提示高併發或需要降低 CPU 負載時採用此架構。

---

*本文摘要基於 vLLM 官方部落格文章，包含架構設計、性能測試結果及部署建議。*
