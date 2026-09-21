# Announcing Native BM25 Ranking in AlloyDB and Cloud SQL

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-19
- **原文連結**: https://cloud.google.com/blog/products/databases/native-bm25-search-in-alloydb-and-cloud-sql/

## 核心主題
Google 宣布在 AlloyDB 和 Cloud SQL 中推出原生 BM25 索引，實現向量搜索與全文搜索的統一混合搜索後端，簡化 AI 應用開發。

## 關鍵重點
- 透過 Tiger Data 的 pg_textsearch 擴展，在 PostgreSQL 17+ 中提供原生 BM25 索引，無需額外全文搜索後端
- 消除數據複製、ETL 管道和同步延遲，實現單一後端的混合搜索，降低運營複雜度
- AlloyDB 用戶可獲得 ScaNN 和 HNSW 索引類型，向量搜索查詢速度提升 6 至 10 倍

## 結論
此功能使 AI 應用開發更簡單、更快，並提供業界標準的關鍵字排名，讓開發者能直接在數據庫內完成混合搜索，無需維護多個後端系統。
---