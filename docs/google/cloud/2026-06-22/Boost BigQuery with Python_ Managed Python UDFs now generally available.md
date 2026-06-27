---
# Boost BigQuery with Python: Managed Python UDFs now generally available

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-22
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/python-udf-in-bigquery-now-generally-available/

## 核心主題
Google Cloud 宣布 BigQuery 正式全面啟用（GA）托管型 Python 使用者自訂函數（Managed Python UDFs），讓資料科學家與工程師能直接在 BigQuery 內部以標準 SQL 查詢執行自訂 Python 程式碼，無需管理任何基礎設施或容器。

## 關鍵重點
- **無伺服器 Python 生態系整合**：BigQuery 自動處理 Python 程式碼的編譯、映像檔建立、安全修補、部署與執行，使用者可直接在 SQL SELECT 子句中引入 NumPy、SciPy、pandas、scikit-learn 等頂尖科學計算庫，或透過 Cloud Resource Connections 安全地呼叫外部 Web API、Cloud Translation、Gemini Enterprise Agent Platform 等服務。
- **高效能進階功能**：GA 版支援以 PyArrow RecordBatches 進行向量化處理，將資料以批次欄位而非逐列方式處理，消除 Python 序列化和轉換開銷，資料密集型計算效能最高可提升 10 倍。使用者可為每個函數配置容器記憶體（最高 16 GB）與 CPU（最高 4 vCPU），並自訂並發請求數（最高 1,000 次同時操作）。
- **完整監控與計費整合**：BigQuery 控制台提供從查詢結果直接連結至 Cloud Monitoring 的即時 CPU、記憶體與並發指標。計費整合至 BigQuery Services SKU，符合 BigQuery 用量承諾折扣（CUDs）資格，並可透過 INFORMATION_SCHEMA.JOBS 及 billing labels（MANAGED_ROUTINE_EXECUTION、MANAGED_ROUTINE_BUILD）進行成本可視性分析。

## 結論
Managed Python UDFs 將 BigQuery 從純 SQL 分析平台擴展為可執行複雜程式邏輯與機器學習工作負載的綜合資料倉儲，讓資料團隊無需跳出 BigQuery 生態系即可運用龐大的 Python 工具鏈。無伺服器架構、向量化處理與完善的計費監控，使其成為企業級生產環境的理想選擇。

---
