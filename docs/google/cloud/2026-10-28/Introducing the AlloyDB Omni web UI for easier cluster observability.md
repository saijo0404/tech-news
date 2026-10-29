# Introducing the AlloyDB Omni web UI for easier cluster observability

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-29
- **原文連結**: https://cloud.google.com/blog/products/databases/alloydb-omni-delivers-a-web-ui-for-cluster-observability/

## 核心主題
Google 正式推出 AlloyDB Omni Web UI，提供生產級、只讀的控制台，讓管理員可直接監控硬體指標、查詢效能與設定旗標，無需離開本地或企業環境即可快速診斷問題。

## 關鍵重點
- **集群概覽與檔案管理**：可快速切換目標連接檔案，無需使用命令列工具
- **系統監控**：即時顯示 CPU、記憶體和磁碟 I/O 的效能指標，協助容量規劃與基礎設施問題排查
- **查詢效能分析**：透過視覺化方式識別資源密集型 SQL 語句，定位延遲瓶頸與慢速查詢
- **列式引擎診斷**：追蹤記憶體使用、快取覆蓋率，驗證分析型查詢加速效果
- **參數與旗標審計**：集中檢查運行時參數，識別與組織基準的設定偏差
- **AlloyDB AI 整合**：可檢視向量搜尋工作流，並快速啟動生態系統工具（如 pgBackRest）
- **生產安全診斷**：介面採用只讀模式，確保診斷會話無法執行寫入命令或修改資料庫設定
- **雙層可觀測性**：整合 Prometheus 即時監控系統硬體指標，自動排名執行密集型 SQL 語句
- **非侵入式監控**：採用最小權限原則，保留現有命令列工具與 CI/CD 流程作為權威控制

## 結論
AlloyDB Omni Web UI 為管理員提供了更輕鬆的集群可觀測性，無需依賴命令列工具，並支援在企業安全邊界和空氣隔開環境中輕鬆部署。管理員可透過此工具快速現代化 PostgreSQL 工作負載，獲得專屬的可觀測性能力。

---