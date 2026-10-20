# How to Use Python UDF Logging for Pipeline Observability

- **來源**: Google Cloud Blog Data Analytics
- **發布日期**: 2026-10-20
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/python-udf-logging-for-pipeline-observability-in-bigquery/

## 核心主題
這篇文章介紹了如何在 BigQuery Python UDF 中使用標準 logging 庫來發結構化日誌到 Cloud Logging，並通過一個電商事件導入管道的實例演示了如何構建容錯和韌性數據管道。

## 關鍵重點
- 開發者現在可以直接在 BigQuery UDF 中使用 Python 標準日誌庫，無需外部插件或自定義連接器即可將結構化日誌發送到 Cloud Logging。
- 文章展示了一個實例，用於在查詢執行期間捕捉行級診斷遥測數據，以便團隊能夠輕鬆隔離問題記錄、觸發實時警報並通過 SQL 解決問題，而無需停止整個工作負載。
- 文章提供了逐步快速入門指南，包括創建通用 Python UDF、啟用日誌的導入、在 Cloud Logging 上設置實時警報以及使用 BigQuery Log Analytics 進行故障排除。
- 文章還涵蓋了其他用例，如陰影執行和安全的遷移、PII 刪紅審計以及 ML 推理漂移，並提供了最佳實踐建議。

## 結論
通過使用 Python UDF 日誌功能，開發者可以實現更強大的數據管道可觀測性，包括實時監控、故障排除和數據恢復，從而提高數據處理的可靠性和靈活性。
