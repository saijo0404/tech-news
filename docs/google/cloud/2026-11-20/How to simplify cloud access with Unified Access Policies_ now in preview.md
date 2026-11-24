# How to simplify cloud access with Unified Access Policies (in preview)

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-21
- **原文連結**: https://cloud.google.com/blog/products/identity-security/how-to-simplify-cloud-access-with-unified-access-policies/

## 核心主題
這篇文章介紹了 Google Cloud 推出的 Unified Access Policies (UAPs)，這是下一代訪問控制引擎，旨在簡化雲端訪問管理並解決傳統 IAM 模型在規模擴展時的限制。

## 關鍵重點
- **統一允許和拒絕語法**：將正則訪問授權和嚴密安全防護合併到單一可審計的政策中，取代了需要對齊的單獨允許和拒絕文件。
- **多綁定支持**：單一 UAP 政策可以綁定最多 25 個 CRM 目標（組織、資料夾和專案），消除了重複的 Terraform 區塊。
- **擴展的規模限制**：UAP 突破了傳統單一政策大小限制，允許將最多 5 個 UAP 政策（每個 64 KB 至多 500 條規則）附加到單一 CRM 資源上，可擴展至 2,500 個唯一主體和每資源 500 個群組。
- **清晰的責任分離**：中央安全架構師可以在組織節點編寫經過驗證的基準和防護政策，並授權資料夾和專案管理員進行自服務綁定，而不讓本地團隊更改中央規則邏輯。
- **原生代理準備**：UAP 將代理視為一等主體（principal://agents.global...），而非通用服務帳戶，允許代理管理員直接為個別代理或整個代理池編寫最小權限允許和拒絕規則。

## 結論
Unified Access Policies 提供了一個更簡單、集中化和可擴展的訪問控制解決方案，幫助平台和安全團隊減少處理權限分散的時間，同時推動業務速度。用戶可以在幾個分鐘內部署第一個政策，並通過 gCloud CLI、REST API 或 Terraform 進行自動化。