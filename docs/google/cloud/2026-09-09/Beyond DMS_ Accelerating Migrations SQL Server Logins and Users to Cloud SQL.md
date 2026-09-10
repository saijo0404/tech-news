# Beyond DMS: Accelerating Migrations SQL Server Logins and Users to Cloud SQL

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-10
- **原文連結**: https://cloud.google.com/blog/products/databases/how-to-replicate-sql-server-logins-and-passwords-to-cloud-sql/

## 核心主題
這篇文章解釋了為什麼 Google Cloud 的 Database Migration Service (DMS) 不會自動複製 SQL Server 登入憑證，以及如何使用 Microsoft 提供的 sp_help_revlogin 腳本來解決這個問題。

## 關鍵重點
- **DMS 不複製登入憑證的原因**：這是為了安全隔離和合規性考量。源環境與目標 Cloud SQL 環境的安全模型不同，自動複製系統登入可能導致未經授權的權限提升，且可能違反 PCI-DSS 或 SOC 2 等合規框架。
- **登入與使用者的區別**：SQL Server 將身份分為兩個層級：登入 (logins) 儲存於 master 資料庫用於驗證連線，使用者 (users) 儲存於個別資料庫用於授權操作。兩者通過唯一的 Security Identifier (SID) 連接。
- **孤獨使用者問題**：當資料庫使用者被複製但對應的伺服器登入不存在或 SID 不匹配時，會導致「孤獨使用者」，使應用程式無法連線。
- **解決方案：使用 sp_help_revlogin**：這是一個 Microsoft 提供的腳本，可以生成包含原始加密密碼哈希和 SID 的 CREATE LOGIN 語句，確保登入憑證完整複製。
- **修復孤獨使用者**：如果不小心創建了登入導致 SID 不匹配，可以使用 `ALTER USER [app_user] WITH LOGIN = [app_user];` 命令重新綁定。
- **進一步現代化**：考慮將 SQL Server 登入遷移至 Customer-Managed Active Directory (CMAD)，採用集中式、企業級的 Kerberos 認證。

## 結論
資料庫遷移不僅是數據遷移，還需要確保應用程式的安全、合規性和可運行情況。雖然 Google Cloud 的 DMS 負責數據複製，但使用 sp_help_revlogin 複製登入憑證是一個簡單且可靠的三步驟過程，可確保無縫切換。

---