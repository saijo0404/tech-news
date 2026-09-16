# Introducing Filestore agent volumes: fully managed storage for agent workspaces

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-16
- **原文連結**: https://cloud.google.com/blog/products/storage-data-transfer/filestore-agent-volumes/

## 核心主題
Google Cloud 推出 Filestore agent volumes，為 AI 代理工作空間提供完全管理的彈性儲存解決方案。

## 關鍵重點
- **自動化管理**：Filestore 自動分配和附著隔離的工作空間，無需手動管理，系統自動處理整個儲存生命週期
- **微秒級恢復**：支援秒級恢復，可節省計算成本並快速恢復，解決傳統儲存供電帶來的冷啟動延遲問題
- **按使用量付費**：根據實際使用量收費，自動將閒置狀態移至低成本儲存層級，避免預先分配固定儲存造成的浪費
- **多代理協作**：支援 Read-Write-Many (RWX) 和 POSIX 檔案鎖定，允許多個代理安全協作，避免檔案衝突

## 結論
Filestore agent volumes 為 AI 代理平台提供高性能、可擴展且成本效益優異的儲存解決方案，可立即開始使用。

---