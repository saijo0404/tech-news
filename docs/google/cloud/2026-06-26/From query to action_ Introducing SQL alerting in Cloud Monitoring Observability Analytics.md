# From query to action: Introducing SQL alerting in Cloud Monitoring Observability Analytics

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-26
- **原文連結**: https://cloud.google.com/blog/products/management-tools/alert-with-sql-in-cloud-monitoring-observability-analytics/

## 核心主題
Google Cloud 在 Cloud Monitoring 的 Observability Analytics 中推出 SQL 警示功能，讓開發者能直接以 SQL 查詢日誌與追蹤資料，並將複雜分析查詢轉為自動化警示，突破傳統監控系統在靈活性與上下文感知上的限制。

## 關鍵重點
- **SQL 警示運作機制**：警示策略會以使用者定義的頻率（例如每 10 分鐘）執行 SQL 查詢，並自動套用「回溯視窗」僅分析上次執行後收到的日誌項目或追蹤跨度。若查詢結果符合設定條件，Cloud Monitoring 會建立事件並透過 Email、Slack 或 PagerDuty 等管道發送通知。查詢透過 BigQuery 處理遥測資料，計費依 BigQuery 標準按需定價或保留專案計算。
- **兩種觸發條件：列數閾值與布林值**：（1）列數閾值（Row count threshold）：當查詢回傳的列數大於、等於或小於設定閾值時觸發，適合「超過 10 名使用者登入失敗」等場景；（2）布林值（Boolean）：當查詢回傳的任何列中特定欄位值為 true 時觸發，可於 SQL 中直接計算百分比等複雜邏輯。範例包含以列數閾值監控支付閘道逾時錯誤（5 分鐘內超過 10 筆觸發），以及以布林值監控 AI 代理程式 p99 延遲（超過 5 秒觸發）。
- **設定步驟與整合能力**：使用前需升級日誌儲存桶至 Observability Analytics、確保 Cloud Trace 資料已收集、建立連結的 BigQuery 資料集，並授予 Monitoring AlertPolicy Editor 與 Logging SQL Alert Writer IAM 角色。在 Google Cloud 控制台的 Observability Analytics 中撰寫驗證 SQL 查詢後，可直接從結果工具列建立警示，也可透過 API 與 Terraform 整合至基礎設施即程式碼（IaC）管線。

## 結論
SQL 警示讓 Cloud Monitoring 從基本閾值監控躍升至深度脈絡感知的檢測層級，能夠計算錯誤百分比、分析高基數維度、以及 JOIN 日誌與追蹤資料。這項功能為開發者與 SRE 團隊提供了前所未有的監控彈性，使關鍵系統問題——如特定客戶錯誤率暴增或與資料庫逾時相關的延遲異常——不再隱藏於聚合訊號中。

---
