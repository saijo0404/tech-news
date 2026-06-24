---
# Boost BigQuery with Python: Managed Python UDFs now generally available

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-22
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/python-udf-in-bigquery-now-generally-available/

## 核心主題
Google Cloud 宣布 BigQuery Managed Python User-Defined Functions（UDFs）正式通用可用（GA），讓資料科學家、工程師與分析師能直接在 BigQuery 內部以標準 SQL 或 BigFrames 執行自訂 Python 程式碼，無需自行管理容器與基礎設施，徹底打通 SQL 與龐大 Python 生態系的連結。

## 關鍵重點
- **全托管無伺服器架構與 Python 生態系整合**：BigQuery 自動處理 Python 程式碼的編譯、映像檔建置、安全修補、部署與執行，使用者只需在 SQL SELECT 子句中呼叫 Python 函式即可。支援 NumPy、SciPy、pandas、scikit-learn 等科學計算套件，並可透過 Cloud Resource Connections 安全地呼叫 Google Cloud 服務（如 Cloud Translation、Gemini Enterprise Agent Platform）或外部 Web API，將資料清理與豐富化直接嵌入查詢流程。
- **進階效能調校與監控能力**：GA 版本提供三大效能優化功能——（1）Pandas PyArrow 向量化處理：直接以 PyArrow RecordBatches 批次處理資料列，避免逐列序列化開銷，資料密集型計算效能提升達 10 倍；（2）可配置容器資源：每函式可配置最高 16 GB 記憶體與 4 vCPU，支援記憶體密集型工作負載（如載入大型序列化模型或地理空間數據）；（3）可自訂並發數：每容器最高支援 1,000 個並發操作，確保平行負載下的成本效益。此外，BigQuery 控制台內建直接連結至 Cloud Monitoring 的即時 CPU、記憶體與並發指標，方便除錯與監控。
- **計費方式與入門資源**：Managed Python UDF 以 BigQuery Services SKU 計費，完全符合 BigQuery 基於支出的使用折扣（CUDs），並可透過 INFORMATION_SCHEMA.JOBS 與 billing labels（MANAGED_ROUTINE_EXECUTION、MANAGED_ROUTINE_BUILD）實現成本可觀測性。使用者可立即從公開 BigQuery 資料集探索已發布的 Python UDF（如使用 o200k_base tokenizer 的分詞函式），或透過 Codelab 進階場景練習，並參考官方文件學習呼叫 Google Cloud 服務與 BigQuery DataFrames 整合。

## 結論
BigQuery Managed Python UDFs 的 GA 發布是 BigQuery 延伸策略的重大里程碑——不再需要為了執行簡單的自訂 Python 函式而維護客製化映像檔與容器，資料團隊能將 Python 工作流直接嵌入資料倉儲的核心。從向量化處理、資源配置到併發優化，這些進階功能讓 Python UDF 不僅可用於原型開發，更足以支撐生產級企業工作負載。隨著計費整合與成本可觀測性的完善，BigQuery 正成為真正的 SQL 與 Python 融合資料分析平台。

---
