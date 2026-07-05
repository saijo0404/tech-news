# How Atlas scales hundreds of merchant databases with Cloud SQL Enterprise Plus edition

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-16
- **原文連結**: https://cloud.google.com/blog/products/databases/how-atlas-scales-hundreds-of-cloud-sql-databases/

## 核心主題
餐廳營運平台 Atlas 為每位商戶配置獨立的 Cloud SQL for PostgreSQL 資料庫，透過升級至 Enterprise Plus edition，解決了連接池管理、查詢效能監控與擴展等營運瓶頸，讓工程師能從基礎設施維護轉而專注產品創新。

## 關鍵重點
- **從標準版到 Enterprise Plus edition 的轉變**：Atlas 最初使用標準 Enterprise 版，隨著商戶增長，連接池需獨立維運、CPU 尖峰時難以定位問題、缺乏專屬資料庫工程師使維護負載倍增。升級至 Enterprise Plus edition 後，連接池整合進 Cloud SQL 原生管理，減少維運組件與安全風險。
- **四大關鍵功能提升營運效率**：（1）內建連接池管理；（2）Query Insights 讓團隊清楚看見哪些商戶的哪些查詢消耗資源，將效能調優從猜測轉為可執行行動；（3）Data Cache 確保讀取效能穩定，即使商戶資料隨日增長；（4）近零停機擴展讓商家成長時可在離峰時段無縫升級。
- **營運成果與 AI 願景**：Atlas 如今服務數千家餐廳門市、每日處理數萬筆訂單，升級後資料庫營運時間減少 30%，新商戶入駐從數天縮短至數秒內完成，團隊能主動預防問題而非被動修復。這讓 Atlas 實現年成長 200% 至 300%，並有足夠信心投入 AI 驅動的餐廳營運工具開發。

## 結論
Cloud SQL Enterprise Plus edition 為 Atlas 提供了靈敏、可觀測且易於擴展的資料庫架構，使團隊能將精力從基礎設施管理轉回商戶服務。在 Google Cloud 承載基礎複雜度的同時，Atlas 得以專注於打造最佳餐廳營運工具，並加速其 AI 驅動的產品創新路徑。

---
