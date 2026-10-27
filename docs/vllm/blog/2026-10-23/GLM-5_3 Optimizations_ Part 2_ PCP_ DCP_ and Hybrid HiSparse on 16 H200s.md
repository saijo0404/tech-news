# GLM-5.3 Optimizations, Part 2: PCP, DCP, and Hybrid HiSparse on 16 H200s

- **來源**: vLLM Blog
- **發布日期**: 2026-10-23
- **原文連結**: https://vllm.ai/blog/2026-10-23-glm53-part2-pcp-dcp-hisparse

## 核心主題
這篇文章介紹了如何在16張H200 GPU上優化GLM-5.3模型，通過Prefill Context Parallelism (PCP)和Decode Context Parallelism (DCP)解決長上下文問題，並使用Hybrid HiSparse技術提升推理效率。

## 關鍵重點
- **PCP (Prefill Context Parallelism)**：將提示分片到每個GPU的token上而非注意力頭，適合GLM-5.3的稀疏注意力機制，大幅降低索引器計算成本，使長提示處理更快速。
- **DCP (Decode Context Parallelism)**：將KV cache按token分片，使1M上下文能放入prefill節點，解決記憶體限制問題。
- **Hybrid HiSparse**：讓decode節點將KV cache保留在主機記憶體中，大幅提升長上下文請求的並發能力。
- **性能提升**：PCP8 × DCP8 prefill搭配Hybrid HiSparse decode在AgentX測試中比數據並行部署快1.7-3.2倍，且是唯一能處理1M上下文配置的方案。

## 結論
這種Prefill/Decode分離架構成功解決了H200上長上下文推理的記憶體和速度限制，特別適合代理工作負載。通過vLLM的Model Runner V2核心，這些複雜的並行策略可以輕鬆組合並正確運行。

---