# How Hugging Face Inference Endpoints, Jobs, and Buckets Power Search on Papers with Code

- **來源**: Hugging Face Blog
- **發布日期**: 2026-08-21
- **原文連結**: https://huggingface.co/blog/pwc-search

## 核心主題
Hugging Face 介紹了如何利用 Inference Endpoints、Jobs 和 Storage Buckets 三項服務構建 Papers with Code 平台的混合搜索系統，使 AI 研究更易于發現和可視化。

## 關鍵重點
- **混合搜索架構**：結合 PostgreSQL 全文搜索與 pgvector 向量搜索，使用 RRF（Reciprocal Rank Fusion）算法組合結果，提升召回率
- **嚴格嵌入合約**：使用 Qwen/Qwen3-Embedding-0.6B 模型，固定版本與 256 維向量，確保嵌入一致性
- **Jobs 批量處理**：利用 GPU 進行大規模論文嵌入（約 75 篇/秒），支持中斷後恢復
- **Buckets 存儲中間件**：作為數據庫、實驗與 Jobs 之間的可靠存儲層，確保可重現性與安全重試
- **Inference Endpoints 即時查詢**：提供低延遲嵌入服務，冷啟動時自動回退到全文搜索
- **系統性能**：110,000+ 論文已嵌入，Recall@20 達 0.9955，查詢延遲 1.31ms (p50)

## 結論
透過將高吞吐量工作（Jobs）與低延遲工作（Inference Endpoints）分離，並以 Storage Buckets 作為可靠存儲層，Hugging Face 成功構建了既強大又快速的混合搜索系統，使 AI 研究更易於發現、比較與擴展。

---

*本文摘要由 AI Agent 自動生成，基於 Hugging Face Blog 於 2026 年 8 月 21 日發布的文章。*
