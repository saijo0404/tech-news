---
# Enhanced data resilience with cross-region backups in Backup and DR Service

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-24
- **原文連結**: https://cloud.google.com/blog/products/storage-data-transfer/backup-and-dr-service-adds-cross-region-backups/

## 核心主題
Google Cloud Backup and DR Service 正式推出跨區域備份功能，將備份目的地與主要工作負載區域解耦，讓組織能以更具成本效益的方式保護資料免受區域性停機影響，同時符合資料駐留法規。

## 關鍵重點
- **備份與來源區域解耦**：跨區域備份讓備份目標可完全獨立於主要工作負載所在的區域，不再綁定於同一區域。此功能已全面支援 Compute Engine 執行個體、磁碟與 Filestore，Cloud SQL 與 AlloyDB 支援將於後續推出。
- **成本優化與合規簡化**：相較於多區域備份的高基礎設施成本，跨區域備份提供更精細的恢復區域選擇，讓組織可針對不同應用程式彈性決定備份策略。同時可精確指定備份存放的地理政治邊界，簡化 GDPR 等資料駐留法規的遵循。
- **簡易三步驟設定**：使用者只需（1）在與來源資源不同的區域建立備份金庫、（2）在資源所在區域建立備份計劃並選擇位於次級區域的金庫、（3）將計劃附加至資源，系統即自動將資料直接傳輸至區域備份金庫，無需額外手動作業。

## 結論
跨區域備份在成本效益與資料韌性之間取得平衡，為需要區域級災難防護但認為多區域備份過度投資的組織提供了理想的解決方案。透過直接備份至次級區域的能力，使用者獲得了比多區域部署更靈活的地理位置選擇自主權，同時維持嚴格的法規合規。

---
