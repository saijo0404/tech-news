# Enterprise-grade PostgreSQL with AlloyDB Omni RPM Orchestrator is generally available

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-10
- **原文連結**: https://cloud.google.com/blog/products/databases/alloydb-omni-rpm-orchestrator-is-generally-available/

## 核心主題
Google 正式推出 AlloyDB Omni Red Hat RPM Orchestrator，提供企業級 PostgreSQL 工作負載的生產級安全性、高可用性與低停機維護能力。

## 關鍵重點
- **四種部署模式**：支援獨立容器（Debian/UBI）、Kubernetes 容器、獨立 RPM 和帶有 RPM Orchestrator 的高可用性企業部署，滿足不同需求。
- **效能提升**：AlloyDB Omni 比標準 PostgreSQL 快 2 倍以上，分析查詢快 100 倍，可 revitalizing 現有基礎設施無需完全遷移。
- **企業合規與安全**：提供 SELinux 強制執行、本地審計日誌等工具，滿足嚴格數據駐留與安全要求。
- **高可用性與讀擴展**：支援讀池（Read Pools）動態擴展讀工作負載，自動處理故障並提供跨區域高可用性。
- **自動化維護與備份**：支援零停機維護、自動備份還原（GCS/S3）、時點恢復（PITR）及動態配置調整。
- **AI 整合能力**：支援向量搜尋、自然語言查詢、AI 函式等 AlloyDB AI 功能，可直接在本地部署 AI 應用。

## 結論
AlloyDB Omni RPM Orchestrator 的正式發布標誌著 Google 將雲端自動化能力直接帶到虛擬機器和裸金屬伺服器，結合高可用性、AI 功能與完全自動化，為企業提供兼具雲端性能與本地控制權限的 PostgreSQL 解決方案。

---