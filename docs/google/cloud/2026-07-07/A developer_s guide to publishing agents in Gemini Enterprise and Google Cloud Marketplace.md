# A developer's guide to publishing agents in Gemini Enterprise and Google Cloud Marketplace

- **來源**: Google Cloud Blog Developers & Practitioners
- **發布日期**: 2026-07-08
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/publish-agents-in-gemini-enterprise-and-google-cloud-marketplace/

## 核心主題
本文提供開發者指南，說明如何將 AI Agent 作為服務（AaaS）發布到 Google Cloud Marketplace 並在 Gemini Enterprise 應用中部署。

## 關鍵重點
- **代理架構設計**：需整合 Google Cloud Marketplace 計費、身份驗證提供者（IdP）安全性以及 Gemini Enterprise Agent Platform，包含客戶專案、合作夥伴專案與合作夥伴 Marketplace 專案三層架構。
- **組織要求**：必須加入 Google Cloud Partner Network、簽署 Marketplace Vendor Agreement，並提供符合 A2A 協議規範的 A2A Agent Card（JSON 檔案），定義代理能力、認證方式與服務端點。
- **技術要求**：代理必須遵循 A2A 協議規範，支援 A2UI 協議以提供互動式使用者介面，並實施 OAuth 2.0 身份驗證或公開訪問，透過 Dynamic Client Registration (DCR) 自動化 OAuth 客戶端註冊流程。
- **發布流程**：在 Producer Portal 中選擇「AI Agent as a Service」解決方案類型，上傳 Agent Card JSON 檔案至 GCS Bucket，設定可用性與定價模型，並完成端到端測試後方可發布。
- **交易管理**：實施採購流程（Google Cloud Marketplace 異步）與註冊流程（Gemini Enterprise 同步），透過 Billing Administrator、Discovery Engine Administrator 與 Discovery Engine User 三個角色確保企業治理合規性。

## 結論
透過使用 Agent Development Kit (ADK) 等工具開始構建，開發者可以將代理擴展至每日工作流中的數百萬企業用戶，加速成長於代理企業時代。

---