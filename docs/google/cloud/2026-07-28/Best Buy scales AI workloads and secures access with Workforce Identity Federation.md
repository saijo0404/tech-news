# Best Buy scales AI workloads and secures access with Workforce Identity Federation

- **來源**: Google Cloud Blog
- **發布日期**: 2026-07-29
- **原文連結**: https://cloud.google.com/blog/topics/retail/best-buy-scales-secure-ai-access-with-workforce-identity-federation/

## 核心主題
Best Buy 透過實施 Google Cloud 的工作人員身份聯結（Workforce Identity Federation）技術，解決了擴展 AI 工作負載時面臨的安全風險和行政摩擦問題。

## 關鍵重點
- **用服務帳戶改為直接聯結**：Best Buy 將原本複雜的服務帳戶管理改為直接使用 Microsoft Entra ID 身份進行認證，消除了服務帳戶金鑰的管理負擔。
- **無同步的無狀態架構**：Workforce Identity Federation 採用無同步、無狀態的架構，在訪問時驗證權限令牌，無需同步用戶記錄。
- **開發者體驗無感且更安全**：開發者只需使用一次企業 Entra ID 憑證即可訪問 BigQuery 等服務，審計日誌顯示個別用戶而非共享服務帳戶身份。

## 結論
Best Buy 透過此架構成功擴展了 AI 工作負載，同時提升了安全性與可管理性，為其他組織提供了可參考的實踐範例。
---