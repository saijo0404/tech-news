# Building the AI-defined vehicle with Android, Google Cloud, and Nexus SDV

- **來源**: Google Cloud Blog
- **發布日期**: 2026-07-14
- **原文連結**: https://cloud.google.com/blog/products/databases/nexus-sdv-uses-bigtable-android-automotive-for-agentic-vehicles/

## 核心主題
Google 透過 Android Automotive SDV 與 Nexus SDV 平台，協助汽車製造商建立 AI 定義的車輛架構，整合 Bigtable 數據庫與 Gemini AI 實現預測性維護與智能車輛功能。

## 關鍵重點
- **AAOS SDV 平台**：採用服務導向架構，將車輛功能解耦為獨立服務，支援動態服務發現，可獨立於主系統運行
- **Nexus SDV 平台**：整合 Bigtable 數據庫，儲存高頻 telematics 數據，支援 AI 代理直接存取數據並觸發自動化工作流
- **AI 代理功能**：Gemini Enterprise 代理可根據駕駛者需求自動調整車輛功能（空調、窗戶、照明等），實現智能車輛體驗
- **預測性維護**：透過 AI 分析車輛數據，提前發現異常並優化維修安排，降低維修成本並提高車輛可用性
- **安全設計**：採用 mTLS、Private GKE 集群與 Secure AI Framework，確保數據隱私與系統安全

## 結論
Nexus SDV 平台提供快速、自動化且安全的車輛架構，幫助汽車製造商超越傳統基礎設施限制，專注於打造獨特的品牌體驗。AI 原生車輛架構將車輛從單純的連接設備轉變為智能、主動的駕駛夥伴。

---

*此摘要已自動生成並儲存至指定檔案路徑。*
