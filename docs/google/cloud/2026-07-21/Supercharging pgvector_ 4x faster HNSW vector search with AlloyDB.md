# Supercharging pgvector: 4x faster HNSW vector search with AlloyDB

- **來源**: Google Cloud Blog
- **發布日期**: 2026-07-22
- **原文連結**: https://cloud.google.com/blog/products/databases/supercharge-pgvector-4x-faster-hnsw-with-alloydb/

## 核心主題
Google 推出 AlloyDB 的列式引擎加速 HNSW 向量搜尋，比標準 PostgreSQL 快 4 倍，同時提升搜尋準確性。

## 關鍵重點
- **性能大幅提升**：對於相同的召回率（例如 0.95），每秒查詢次數（QPS）可提升 4.2 至 4.9 倍，允許在同一硬體上處理更多並行向量搜尋。
- **搜尋準確性提升**：在固定 QPS 水平下，召回率從約 0.78 提升至超過 0.94，提升 0.163，使 AI 應用獲得更準確的結果。
- **無需應用程式修改**：這些性能提升是內建於 AlloyDB 的，使用標準 pgvector SQL 語法即可獲得，無需修改應用程式。

## 結論
AlloyDB 的列式引擎加速 HNSW 不僅僅是更快的資料庫，還能降低基礎設施成本並提高 AI 準確性。對於企業級應用，這是在速度和準確性之間取得最佳平衡的關鍵解決方案。

---