# Multiple result sets: How Database Migration Service automates SQL server to PostgreSQL translation

- **來源**: Google Cloud Blog
- **發布日期**: 2026-08-05
- **原文連結**: https://cloud.google.com/blog/products/databases/automating-postgres-translations-with-database-migration-service/

## 核心主題
這篇文章介紹了 Google Cloud 的 Database Migration Service (DMS) 如何自動化將 SQL Server 的多結果集存儲程序轉換為 PostgreSQL 函數或存儲程序，解決大規模數據庫遷移中的結構性挑戰。

## 關鍵重點
- DMS 根據結果集數量（單一或多個）以及是否使用標量返回值，自動決定將 SQL Server 存儲程序轉換為 PostgreSQL 的 STORED PROCEDURE 或 FUNCTION
- 對於單一結果集或僅有標量返回值的程序，使用 INOUT refcursor 參數；對於多個結果集或組合的情況，轉換為 RETURNS SETOF refcursor 函數
- 應用端需要適應新的游標處理方式，在 PostgreSQL 中必須使用 BEGIN...COMMIT 塊來處理游標數據
- DMS 使用深度優先搜索 (DFS) 算法分析程序調用圖，準確計算結果集數量並處理動態情況

## 結論
理解這種自動化架構有助於開發團隊準確解析多層級響應數組，確保在 PostgreSQL 中實現無縫的二天運營。

---