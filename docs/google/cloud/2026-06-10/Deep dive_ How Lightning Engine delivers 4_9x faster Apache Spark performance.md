---
# Deep dive: How Lightning Engine delivers 4.9x faster Apache Spark performance

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-10
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/lighting-engine-for-apache-spark-performance-deep-dive/

## 核心主題
Google Cloud 宣布 Lightning Engine for Managed Service for Apache Spark 正式全面可用，透過向量化原生執行、雲端儲存與 BigQuery 連接器最佳化，以及進階查詢最佳化，在零程式碼修改的前提下提供最高 4.9 倍於標準開源 Spark 的效能提升。

## 關鍵重點
- **向量化原生執行核心**：Lightning Engine 基於開源 Gluten 與 Velox 運行時並加入 Google 專屬增強，將 Spark 物理查詢計畫編譯為最適化 SIMD 向量化指令的 C++ 原生程式碼，涵蓋向量化排序（原生記憶體中(columnarly)處理資料列以降低 CPU 週期開銷）、加速視窗函數（直接在原生 C++ 層執行移動平均、聚合與去重計算），以及智慧降級機制（遇到未支援的操作符或 Java UDF 時自動將子樹退回 JVM 執行，避免不必要的格式轉換）。
- **雲端儲存與 BigQuery 連接器最佳化**：包括直接路徑連線（繞過多節點中繼跳轉，以雙向串流與 Cloud Storage 通訊，使 seek 操作與向量化 readV API 無需重新開啟串流即可執行，加速深度巢狀 Parquet/ORC 檔案掃描）、元資料呼叫減少（在驅動端使用字典序列出收集元資料並直接傳輸至執行器，消除冗餘 Cloud Storage API 呼叫），以及原生 BigQuery 連接器（以 Arrow 格式直接消費 BigQuery 資料，避免昂貴的 Arrow 至 JVM UnsafeRow 轉換）。
- **廣播 joins 與進階查詢最佳化**：採用受 Google F1 與 Spanner 查詢引擎啟发的成本基礎查詢最佳化器，包含單一 HashTable 快取（在標準廣播 join 中每 executor 只建立一次 join hash table 並快取，消除重複 CPU 週期）、聚合降級（自動將部分聚合推入 join shuffle 下方以減少網路傳輸量），以及自動 shuffle 分區（基於執行階段統計數據動態決定每個查詢階段的最適 shuffle 分區數，避免 OOM spill 與過度分區）。

## 結論
Lightning Engine 已在超過一百萬個真實工作負載中驗證，提供工業級穩定性與可靠效能增益（價格效能為主流高速 Spark 替代方案的 2 倍），並支援無伺服器與受管理叢集兩種部署模式；使用者可透過 Google Cloud Console 或 gcloud CLI 直接啟用，實現零程式碼修改的 Spark 查詢加速。

---
