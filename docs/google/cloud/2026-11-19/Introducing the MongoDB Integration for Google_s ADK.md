# Introducing the MongoDB Integration for Google's ADK

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-20
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/introducing-the-mongodb-integration-for-googles-adk/

## 核心主題
Google 推出了 MongoDB 與 Google Agent Development Kit (ADK) 的整合，讓開發者可以輕鬆建立具備持久化記憶與會話管理的 AI 代理，無需額外設定獨立資料庫。

## 關鍵重點
- **MongoDBSessionService**: 提供會話持久化功能，可將應用程式、使用者與會話層級的狀態儲存至 MongoDB，確保多輪互動中的上下文保留。
- **MongoDBMemoryService**: 支援長期記憶功能，透過關鍵字匹配召回相關記憶，並具備重複加入防護機制。
- **MongoDB Search**: 提供資料檢索能力，讓代理能即時存取產品目錄、文檔與記錄，支援向量與混合檢索。
- **單一平台架構**: 整合後無需額外設定向量資料庫或搜尋引擎，降低延遲並簡化部署。
- **支援 MongoDB Atlas 與自管理 MongoDB 8.0+**，提供彈性部署選項。

## 結論
此整合讓開發者能以原生開發者體驗，快速將代理從原型階段轉化為生產環境，同時提供安全、可靠的資料存取與記憶管理，無需額外系統整合。

---