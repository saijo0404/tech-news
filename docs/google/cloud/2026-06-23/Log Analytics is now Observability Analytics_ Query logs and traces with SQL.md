# Log Analytics is now Observability Analytics: Query logs and traces with SQL

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-23
- **原文連結**: https://cloud.google.com/blog/products/management-tools/query-logs-and-traces-with-sql-in-observability-analytics/

## 核心主題
Google Cloud 宣布 Log Analytics 正式升級為 Observability Analytics，並將 Trace 資料與 Observability API 推向通用（GA）版本，透過 SQL 將日誌（logs）與追蹤（traces）整合至單一分析平台，讓開發者與 SRE 能跨維度查詢與關聯分散式系統的可觀測性數據。

## 關鍵重點
- **Observability Analytics 核心能力**：前身為 Log Analytics，現將 BigQuery 與 SQL 的強大查詢能力直接引入 Cloud Observability，允許開發者在單一位置以 SQL 關聯高流量日誌與追蹤數據，無需遷移或重複儲存資料。三大優勢包括：（1）統一可觀測數據——以 SQL 查詢並 JOIN 日誌與追蹤數據；（2）業務關聯分析——將可觀測性資料與 BigQuery 中的業務數據（如轉換率、營收、營運成本）關聯，量化技術問題的商業影響；（3）就地分析——直接在 Cloud Logging 與 Cloud Trace 內分析數據，降低重複匯出儲存成本與複雜度。
- **AI Agent 優化與客戶延遲影響分析兩大實例**：（1）AI Agent 工具失敗與延遲分析——Agent 常執行多步驟外部工具呼叫（資料庫查詢、網頁搜尋、API 呼叫等），透過 Observability Analytics 可在數百萬 span 事件中執行聚合查詢，計算每個工具的失敗率與 P95 延遲，快速定位瓶頸（如某工具 P95 延遲 8 秒需優化資料庫索引）或發現不穩定工具（如 15% 失敗率暗示 API 速率限制問題）；並可進一步 JOIN 應用日誌提取導致失敗的 LLM 提示與推理過程。（2）客戶延遲影響分析——即使追蹤屬性中未傳播使用者或客戶 ID（因隱私或技術原因），只要應用存取日誌中有記錄，即可 JOIN traces 與 logs 找出受最差效能影響的客戶。
- **Observability Analytics 頁面與 Log/Trace Explor器的定位差異，以及 AI Agent 程式化查詢支援**：Cloud Logging 與 Trace 仍保留各自的 Explorer 工具，適合尋找與檢查單一日誌或追蹤記錄；Observability Analytics 則專注於聚合與深度分析，用於回答服務級別的廣泛問題（如「上週結帳服務 P95 延遲為何？」「最近部署後錯誤率最高的 API 端點為何？」）。同時，Observability API（現為 GA）支援建立與 Observability Buckets 關聯的 BigQuery 資料集，讓 AI Agent 或分析工作負載能直接透過 BigQuery API 程式化查詢數據。

## 結論
Observability Analytics 的升級與 Trace SQL 支援打破了日誌與追蹤資料的孤島，將可觀測性從「單筆記錄檢索工具」提升至「跨維度聚合分析平台」。對傳統工作負載而言，它能量化技術問題對業務的財務影響；對 AI Agent 而言，它能以 SQL 在數百萬次執行中快速定位最常失敗的工具與效能瓶頸。結合可程式化的 Observability API，Google Cloud 讓開發者、SRE 與 AI Agent 都能以更高效的方式診斷問題、優化系統並理解技術決策的商業意義。

---
