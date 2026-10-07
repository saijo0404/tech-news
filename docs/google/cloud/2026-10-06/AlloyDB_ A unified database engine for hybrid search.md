# AlloyDB: A unified database engine for hybrid search

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-06
- **原文連結**: https://cloud.google.com/blog/products/databases/simplify-ai-search-with-alloydb-hybrid-search-and-rrf/

## 核心主題
這篇文章介紹了 AlloyDB AI 如何通過原生混合搜索功能，簡化 AI 搜索應用，整合向量搜索與全文搜索，並提供 RUM 擴展、BM25 索引和外部搜索 FDW 等創新功能。

## 關鍵重點
- **RRF 混合搜索**: 使用 Reciprocal Rank Fusion (RRF) 將複雜的多步驟搜索流程簡化為單一 SQL 函數調用，消除複雜的評分歸一化需求。
- **RUM 擴展**: 引入 RUM 擴展，通過存儲詞語位置信息實現低延遲全文搜索，解決 GIN 索引的效能瓶頸。
- **BM25 索引**: 提供原生 BM25 索引，帶來行業標準的關鍵字評分精度，無需外部搜索引擎。
- **外部搜索 FDW**: 通過 Foreign Data Wrapper 支持 Elasticsearch、OpenSearch 和 Solr 等外部集群，擴展搜索靈活性。

## 結論
AlloyDB AI 通過統一平台解決現代搜索的架構複雜性問題，為 AI 應用提供高性能且易維護的搜索基礎設施，讓開發者能專注於應用功能開發而非搜索架構維護。
---

檔案已成功儲存。