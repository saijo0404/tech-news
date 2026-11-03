# Beyond Migration: Using Database Migration Service for disk shrinking

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-03
- **原文連結**: https://cloud.google.com/blog/products/databases/use-dms-to-shrink-cloud-sql-for-sql-server-disk/

## 核心主題
這篇文章介紹了如何使用 Google Cloud 的 Database Migration Service (DMS) 來以最小化停機時間的方式縮小 Cloud SQL for SQL Server 的磁碟空間。

## 關鍵重點
- DMS 支援將 Cloud SQL for SQL Server 作為來源，可實現持續、低停機時間的資料庫複製
- 當資料庫儲存空間只增加時，DMS 可作為日常工具用於儲存管理，特別是執行磁碟縮小操作
- 透過將工作負載複製到新的小型磁碟實例，可在應用程式運行中完成磁碟縮小，只需短暫切換窗口
- 需要手動遷移伺服器級別物件（如登入、SQL Server Agent 任務、連結伺服器）
- 切換後需要處理遺棄的資料庫使用者問題

## 結論
DMS 不僅是上雲的橋樑，更是 Cloud SQL 工程師日常操作工具包中的多功能工具，特別適合生產環境 SLA 嚴格、無法接受長時間停機維護的場景。
---