---
# Boost BigQuery with Python: Managed Python UDFs now generally available

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-22
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/python-udf-in-bigquery-now-generally-available/

## 核心主題
Google Cloud 宣布 BigQuery Managed Python UDF 正式通用（GA），讓資料科學家、工程師與分析師能直接在 BigQuery 中以標準 SQL 或 BigFrames 執行自訂 Python 程式碼，無需管理基礎設施或容器，徹底打破純 SQL 在處理複雜邏輯時的限制。

## 關鍵重點
- **SQL 與 Python 生態系的橋樑**：Python UDF 運行於 BigQuery 管理的 serverless 資源上，自動縮放至數十億行資料，BigQuery 自動處理編譯、映像檔建置、安全更新、部署與執行。核心優勢包括：（1）彈性——在 SQL SELECT 子句中直接存取 NumPy、SciPy、pandas、scikit-learn 等頂尖 Python 函式庫；（2）外部 API 整合——在查詢內安全呼叫 Google Cloud 服務（如 Cloud Translation、Gemini Enterprise Agent Platform）或自訂微服務；（3）全托管 serverless——無需設定基礎設施或管理容器。
- **進階效能與資源調控**：支援 PyArrow RecordBatches 向量化處理，以批次處理取代逐列操作，將序列化與轉換開銷降至最低，效能提升高達 10 倍；可配置容器資源（記憶體高達 16 GB、CPU 高達 4 vCPU）以執行記憶體密集型工作負載；自訂並發設定（每容器高達 1,000 次並行請求）以最佳化吞吐量；內建即時監控，可透過 Cloud Monitoring 直接查看 CPU、記憶體與並行指標。
- **計費與開始使用**：Python UDF 以 BigQuery Services SKU 計費，可適用 BigQuery 承諾使用折扣（CUDs）；透過 INFORMATION_SCHEMA.JOBS 與 billing labels（MANAGED_ROUTINE_EXECUTION、MANAGED_ROUTINE_BUILD）實現成本可觀測性。提供公共資料集預先發布的範例函式、Code Lab 教學，以及 BigQuery DataFrames（BigFrames）與 Google Cloud 服務串接的完整文件。

## 結論
BigQuery Managed Python UDF 的 GA 是 BigQuery 擴展策略的重大里程碑——將 Python 的豐富生態系直接帶入資料倉儲核心，讓開發者不再需要為了簡單函式而額外管理容器與計算資源。搭配向量化處理、可調控資源與完整的監控工具，這套功能讓資料團隊能在同一個平台上完成從資料清洗、科學計算到機器學習預處理的完整工作流程。

---
