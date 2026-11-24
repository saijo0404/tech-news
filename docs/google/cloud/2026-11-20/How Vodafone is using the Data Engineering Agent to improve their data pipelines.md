# How Vodafone is using the Data Engineering Agent to improve their data pipelines

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-21
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/vodafone-cuts-data-pipeline-costs-30-via-data-engineeringagent/

## 核心主題
Vodafone 使用 Google Cloud 的 Data Engineering Agent 將遺留的 BigQuery 儲存程序現代化為模組化 Dataform 管道，成功將管道執行時間縮減一半並降低 30% 的成本。

## 關鍵重點
- **遺留系統現代化**: Vodafone 原本使用大量複雜的 BigQuery 儲存程序進行資料轉換，這些程式碼龐大且難以維護。透過 Data Engineering Agent，他們成功將這些儲存程序轉換為模組化的 Dataform 管道。
- **平行化與效能提升**: Data Engineering Agent 將程式碼平行化為獨立步驟，大幅提升可讀性和執行效率。新管道執行速度是舊系統的兩倍。
- **成本降低 30%**: 透過讓 Agent 儲存中間表格（使用 BigQuery 實體化視圖），Vodafone 成功將資料管道成本降低 30%。
- **自動化測試與依賴管理**: 新管道具備自動測試功能和基於依賴關係圖的自動執行，取代了手動調試和依賴管理。
- **90% 遷移時間縮減**: 相比傳統手動方法，Agent 協助的遷移時間大幅縮減 90%，大幅降低工程人員的重複性工作。

## 結論
Data Engineering Agent 不僅幫助 Vodafone 成功現代化資料管道架構，還顯著提升了效能並降低了成本。這項經驗證明了 AI 代理工具在資料工程領域的巨大潛力，未來 Vodafone 計劃將此工具擴展至更多市場和專案中。
---