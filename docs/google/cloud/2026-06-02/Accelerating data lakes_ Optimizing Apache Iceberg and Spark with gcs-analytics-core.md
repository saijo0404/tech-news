# 加速資料湖：利用 gcs-analytics-core 最佳化 Apache Iceberg 與 Spark

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-02
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/optimize-iceberg-and-spark-workloads-with-gcs-analytics-core/

## 核心主題
Google 開源推出 gcs-analytics-core Java 程式庫，作為 Analytics Engine 與 GCS Java SDK 之間的集中式效能優化層，為 Apache Iceberg、Spark 等資料處理框架提供無縫的 GCS 讀取效能提升，無需任何自訂調校即可自動受益。

## 關鍵重點
- **兩大核心技術優化：向量化 I/O 與 Smart Parquet 預取**：Vectored I/O（多執行緒）讓系統能在單一操作中平行擷取多個資料範圍，取代傳統逐一發出的網路呼叫，大幅降低 GCS 呼叫開銷與檔案開啟延遲；Smart Parquet Prefetching 自動將 Parquet 檔案的 footer 元資料（通常 50KB-100KB）以單一資料塊預取，避免引擎反覆後seek 擷取中繼資料造成的多次網路請求。
- **Apache Iceberg 深度整合與 TPC-DS 壓測數據**：gcs-analytics-core 已原生整合至 Iceberg Java runtime 1.11.0 版以上的 GCSFileIO 實作中，所有 Iceberg catalog（REST catalog、Hive 等）自動享有 Parquet footer 預取與多執行緒向量化讀取，無需調整現有架構設定；TPC-DS 基準測試（1GB 至 10TB 資料集）顯示掃描時間改善幅度從 18.40%（10TB）至 71.51%（1GB），整體執行時間改善從 1.58%（10TB）至 32.61%（1GB），證實 I/O 瓶頸紓解能直接降低查詢總執行時間。
- **開源與快速上手指南**：程式庫於 GitHub 開源（GoogleCloudPlatform/gcs-analytics-core），使用方式僅需四步驟——安裝 Iceberg Spark runtime 1.11.0+、配置 GCSFileIO、啟用 `gcs.analytics-core.enabled=true` 優化旗標、開啟 `iceberg.vectorization.enabled=true` 向量化 I/O；開發者可透過內建的微基準測試與設計文件貢獻程式碼或驗證效能。

## 結論
gcs-analytics-core 將 Google 對 GCS 的效能最佳化經驗封裝為可重複使用的開源程式庫，以「集中式優化層」取代過去分散在各框架中的特定調校，讓資料工程師從繁複的效能排障中解放，專注於查詢邏輯本身——資料湖的讀取效能不再受限於 I/O，計算引擎能將更多時間花在真正需要的事上。
