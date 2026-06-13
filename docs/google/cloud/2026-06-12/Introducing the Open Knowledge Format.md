# 引入開放知識格式（Open Knowledge Format）

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-12
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/how-the-open-knowledge-format-can-improve-data-sharing/

## 核心主題
Google Cloud 發布開放知識格式（OKF）v0.1，一個將「LLM Wiki」模式正式化為可攜式、跨平台標準的開放規格，讓不同組織與系統能無縫共享 AI 系統所需的情報、上下文與知識。

## 關鍵重點
- **解決知識碎片化問題**：企業內部知識散落在元資料目錄、Wiki、程式碼註解、筆記本單元與資深工程師腦中，AI 代理在回答問題時必須自行拼湊互不相容的資訊來源；OKF 以目錄結構的 Markdown 檔案搭配 YAML frontmatter 統一知識表示方式，無需專屬 SDK 或運行時即可讀取、索引與傳輸。
- **三大設計原則**：（1）最小化干預——每個概念只需一個 `type` 欄位，其餘欄位與內容結構由生產者自由決定；（2）生產者/消費者獨立——人類手寫知識可由 AI 代理消費，機器匯出的知識可由人類瀏覽，格式是合約而工具可獨立替換；（3）格式而非平台——OKF 不綁定任何雲端、資料庫或 AI 框架，永遠不需要專屬帳號即可讀寫。
- **參考實作與生態開源**：Google 發布了 BigQuery 資料表自動產生 OKF 概念的富化代理、單一 HTML 靜態圖形視覺化工器，以及 GA4 電商、Stack Overflow、Bitcoin 三個範例 bundles；Google Cloud Knowledge Catalog 已支援 OKF 匯入，規格與實作開源於 GitHub，歡迎社群貢獻替代實作與擴充。

## 結論
OKF 以「Markdown + YAML frontmatter」這個極簡形式，為 AI 時代的知識共享建立了一種通用語言，讓知識不再被封鎖在特定工具或組織內部，而是能在版本控制中與程式碼共存、跨產品流通，為代理式 AI 系統提供可靠且可互操作的上下文基礎。
