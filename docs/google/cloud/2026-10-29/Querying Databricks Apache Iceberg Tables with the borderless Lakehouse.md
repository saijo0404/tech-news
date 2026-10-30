# Querying Databricks Apache Iceberg Tables with the borderless Lakehouse

- **來源**: Google Cloud Blog Data Analytics
- **發布日期**: 2026-10-30
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/querying-databricks-iceberg-tables-with-google-clouds-lakehouse/

## 核心主題
這篇文章介紹了如何使用 Google Cloud 的 Lakehouse 框架直接查詢 Databricks 管理的 Apache Iceberg 表格，實現零複製數據的跨平台分析。

## 關鍵重點
- **零複製查詢**：BigQuery 可以直接讀取 Databricks 寫入的 Iceberg 表格，無需複製數據，降低存儲成本
- **跨雲分析**：支持從 Google Cloud、AWS S3、Azure Blob 等外部存儲直接查詢，實現真正的多雲分析
- **分區剪枝優化**：利用 Iceberg 元數據優化查詢，只讀取相關數據文件，減少運算資源消耗
- **集中式安全治理**：通過 delegated access 實現集中化的訪問控制和安全管理，避免分散式系統的安全漏洞
- **定期維護管理**：需要定期執行 compaction 和 VACUUM 操作來優化性能，避免小文件問題和遺棄文件

## 結論
這種零複製架構讓企業能夠在不遷移數據的情況下，將 Databricks Iceberg 數據集與 BigQuery 連接，實現可擴展的工程工作負載和並行分析。通過 Lakehouse 聯邦、緩存機制和定期維護，可以構建高效、零複製的湖倉架構，降低存儲開銷並為現代分析工作負載和 AI 工作負載做好準備。

---