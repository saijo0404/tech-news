# What's new with Google Data Cloud

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-04
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/whats-new-with-google-data-cloud/

## 核心主題
Google Data Cloud 團隊回顧 2026 年 1 月至 9 月的產品更新，涵蓋 BigQuery、Dataflow、Looker、Firestore 等數據分析、BI 和資料庫服務的最新功能。

## 關鍵重點
- **BigQuery 連續查詢支援狀態處理**：新增 JOIN、聚合和窗口函數功能，可計算時間序列指標（如 30 分鐘平均值），為下游應用和 AI 代理提供更豐富的即時訊號。
- **Kafka 管理服務新增合成資料生成工具**：只需 3 次點擊即可向 Kafka 集群發送模擬資料，2 分鐘內完成資料流測試，無需修改客戶端應用或啟動虛擬機。
- **Dataflow 管道更新功能更靈活**：支援停止並替換管道，新增並行管道選項加速遷移，並可設定排水超時時間以防止 runaway 成本。
- **Lakehouse 新增 Apache Iceberg 管理表**：消除 BigQuery 與開源引擎間重複資料管道的維護負擔，提供原生多引擎讀寫互操作性，內建自動化表管理（壓縮和分區調整）。
- **Airflow 3.1 正式推出**：包含 AI 驅動的代理排錯功能，可在 Cloud Composer 中直接調查失敗任務，自動分析日誌並提供解決方案建議。
- **BigQuery Graph 推出**：提供易於使用的高擴展性圖分析解決方案，可建模、分析和視覺化大規模關係。
- **Data Studio 重新推出**：擴展至 BigQuery 對話式代理和 Colab 筆記本中的資料應用，融入 AI 時代。
- **Looker 新增對話式分析**：支援自訂資料驅動應用，透過 Gemini 提供自然語言體驗，並推出自服務 Explores 功能。
- **Firestore Enterprise 重構**：新增管道操作功能，包含 100 多個新查詢功能、無索引查詢和新索引類型，支援無縫遷移。
- **推出 BigQuery 自建的 ODBC 和 JDBC 驅動**：提供直接高效能連接，完全由 Google 開發。
- **Microsoft Entra ID 整合 Cloud SQL**：支援 SQL Server 2022，提供集中式身份管理、多因素認證和簡化用戶管理。
- **Cloud SQL 自動擴展讀池**：可動態調整讀取能力，支援多個讀副本通過單一讀端點訪問。

## 結論
Google Data Cloud 持續強化 AI 整合能力，透過語意層和 AI 代理讓資料分析更直覺化。客戶如 Telenor、Intel、Carousell 等已利用這些功能將資料轉化為行動，推動主要商業和技術突破。

---