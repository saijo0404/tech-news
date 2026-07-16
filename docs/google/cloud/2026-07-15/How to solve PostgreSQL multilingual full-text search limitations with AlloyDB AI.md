# How AlloyDB overcomes indexing limitations with AI functions

- **來源**: Google Cloud Blog
- **發布日期**: 2026-07-16
- **原文連結**: https://cloud.google.com/blog/products/databases/how-alloydb-overcomes-indexing-limitations-with-ai-functions/

## 核心主題
AlloyDB 利用 Gemini AI 函數解決中文等連續文字的分詞限制，提供企業級多語言全文搜尋能力。

## 關鍵重點
- 傳統 PostgreSQL 索引無法處理中文等無空格語言的分詞問題，標準分詞器會將整句視為單一關鍵字
- AlloyDB AI Functions 可將 Gemini 模型直接整合到資料庫中，實現資料內 AI 處理，無需外部 ETL 管道
- 使用 PL/pgSQL 儲存程序配合陣列批量處理，解決大規模資料處理時的鎖定、滾回和同步問題
- 支援 RUM 全文搜尋索引與 ScaNN 向量搜尋的混合搜尋，提供精確的關鍵字與語意搜尋結果

## 結論
AlloyDB AI 提供企業級多語言全文搜尋解決方案，透過原生資料庫 AI 函數避免資料移動風險，同時結合 ScaNN 向量搜尋技術實現高效能的混合搜尋，無需維護複雜的外部搜尋引擎架構。

---