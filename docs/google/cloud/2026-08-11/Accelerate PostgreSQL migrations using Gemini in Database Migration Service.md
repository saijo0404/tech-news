# Accelerate PostgreSQL migrations using Gemini in Database Migration Service

- **來源**: Google Cloud Blog
- **發布日期**: 2026-08-12
- **原文連結**: https://cloud.google.com/blog/products/databases/accelerate-postgresql-migrations-with-gemini-in-dms/

## 核心主題
這篇文章介紹了 Google 的 Database Migration Service (DMS) 如何利用 Gemini AI 來加速將 Oracle 或 SQL Server 等商業資料庫的儲存程序、觸發器和自訂函數轉換為 PostgreSQL PL/pgSQL 代碼，解決資料庫遷移中的「最後一哩路」瓶頸。

## 關鍵重點
- **全資料庫上下文分析**: Gemini 在 DMS 中不僅分析代碼片段，還分析整個資料庫上下文，包括表關係、資料類型、依賴視圖和跨程序引用，確保轉換的準確性。
- **企業級安全與隱私**: 代碼轉換嚴格在 Google Cloud 專案邊界內運行，符合 IAM 治理規範，保護專有業務邏輯和知識產權。
- **整合執行工作區**: DMS 消除了跨數百個文件的複製粘貼工作，允許用戶在單一控制台內審查並行代碼差異、檢查內聯 AI 解釋、編輯代碼並將驗證後的 PL/pgSQL 例程直接部署到目標資料庫。
- **確定性準確性與 AI 編譯**: DMS 將確定性編譯器規則（用於 1:1 映射，如標準 DDL 轉換、標量函數和定義良好的語法轉換）與 Gemini 的上下文綜合用於複雜的程序塊，確保精確、可預測的翻譯，避免模型漂移。
- **Oracle PL/SQL 到 PostgreSQL 轉換示例**: 文章提供了具體示例，展示如何將 Oracle PL/SQL 中的 NVL 函數轉換為 PostgreSQL 的 COALESCE，以及 DECODE 函數轉換為 CASE 表達式，並提供內聯解釋。

## 結論
透過 Gemini 輔助的代碼轉換，資料庫團隊可以在幾天內完成原本需要數月的遷移工作，大幅降低人工成本並提高轉換準確性。建議資料庫團隊使用 Database Migration Service 控制台啟動遷移評估，以開始資料庫轉換流程。

---