# BigQuery ObjectRef now GA: Build multimodal data platforms for conversational analytics entirely in SQL

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-22
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/analyze-unstructured-data-in-bigquery-with-objectref/

## 核心主題
BigQuery 正式推出 ObjectRef 功能，允許將非結構化數據（如圖片、視頻、音頻、文檔）作為原生 ObjectRef 欄位直接儲存於 BigQuery 表格中，並透過單一 SQL 查詢即可結合多模態輸入進行 Gemini 模型分析。

## 關鍵重點
- **ObjectRef 架構優勢**：ObjectRef 是預定義的 STRUCT 資料類型，可將非結構化檔案視為一等公民資料，並支援零複製架構、SQL/Python 互操作性、獨立生命週期與版本控制。
- **完整 ETL 流程**：可透過 SQL 直接進行資料清洗、分類、標註等作業，並保留原始 ObjectRef 與分析結果在同一行，實現雙層分析。
- **GA 新功能**：新增終端使用者憑證 (EUC) 支援、統一支援 Cloud Storage 元資料來源、以及陣列支援以進行比較分析。
- **實際應用案例**：Snap 利用此功能提升內容審查效率；企業可透過此架構進行內容審查、威脅偵測、庫存合規與客戶體驗分析。

## 結論
BigQuery 透過 ObjectRef 實現了結構化與非結構化數據的統一處理，使數據工程師能利用大語言模型直接在 SQL 中完成多模態分析，無需額外計算資源，大幅降低營運成本並提升分析效率。

---