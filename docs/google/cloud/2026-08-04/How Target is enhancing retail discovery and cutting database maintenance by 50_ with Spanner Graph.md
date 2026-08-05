# How Target is enhancing retail discovery and cutting database maintenance by 50% with Spanner Graph

- **來源**: Google Cloud Blog
- **發布日期**: 2026-08-05
- **原文連結**: https://cloud.google.com/blog/topics/retail/how-target-rebuilt-retail-discovery-with-spanner-graph/

## 核心主題
Target 透過導入 Spanner Graph 統一其分散的數據架構，實現更個人化的零售發現體驗，並將基礎設施維護成本降低 50%。

## 關鍵重點
- **統一數據平台**：整合搜尋、向量、交易數據與圖關係，取代原本分散的 Elasticsearch 與 NoSQL 資料庫
- **企業本體建構**：建立「圖之圖」架構，支援多跳圖遍歷、向量相似度搜尋與全文關鍵字查詢
- **零停機遷移**：透過四階段策略（架構映射、數據整合、Canary 部署、切換清理）實現平滑遷移
- **業務效益**：推薦相關性提升、Net Promoter Score 改善、開發人員基礎設施維護時間減少 50%

## 結論
Spanner Graph 不僅解決了 Target 的數據碎片化問題，更成為 GraphRAG 基礎設施的核心，加速了其生成式 AI 路線圖，為零售業提供了可複製的架構轉型範例。

---