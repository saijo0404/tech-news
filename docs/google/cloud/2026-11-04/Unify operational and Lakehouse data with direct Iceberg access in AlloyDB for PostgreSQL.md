# Unify operational and Lakehouse data with direct Iceberg access in AlloyDB for PostgreSQL

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-05
- **原文連結**: https://cloud.google.com/blog/products/databases/direct-iceberg-access-in-alloydb/

## 核心主題
Google Cloud 推出直接 Iceberg 存取功能，讓 AlloyDB for PostgreSQL 能直接查詢 Apache Iceberg 表格，並將營運數據與分析數據整合。

## 關鍵重點
- **直接 Iceberg 存取**：AlloyDB 可直接從雲端儲存桶讀取 Apache Iceberg 表格，並與即時營運數據進行單一 SQL 查詢，查詢速度比 Amazon 可比對服務快 7 倍
- **AlloyDB sync**：一般化推出，可將 BigQuery 數據同步到 AlloyDB，供低延遲工作負載使用，可設定刷新頻率
- **Lakehouse federation**：一般化推出，允許 AlloyDB 直接查詢 BigQuery 表格，由 BigQuery 處理大部分處理工作，並可設定計費專案與權限控制

## 結論
這些新功能讓應用程式和 AI 代理能夠在無需建立或管理自訂管道的情況下，同時對營運和湖式數據進行操作，實現決策的即時性。Etsy 已利用此架構將數據整合 3 PB，加速管道查詢 60%。

---