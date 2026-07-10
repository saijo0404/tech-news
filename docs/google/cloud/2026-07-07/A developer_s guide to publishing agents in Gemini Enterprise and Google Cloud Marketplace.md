# A developer's guide to publishing agents in Gemini Enterprise and Google Cloud Marketplace

- **來源**: cloud.google.com/blog
- **發布日期**: 2026-07-08
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/publish-agents-in-gemini-enterprise-and-google-cloud-marketplace/

## 核心主題
這篇文章提供開發者指南，說明如何將 AI 代理發布到 Google Cloud Marketplace 和 Gemini Enterprise 應用，包括架構設計、認證要求、技術整合和交易管理流程。

## 關鍵重點
- 開發者需遵循 A2A 協議標準，建立符合 A2UI 協議的互動介面，並提供 A2A Agent Card（JSON 檔案）宣告代理能力、認證方法和服務端點
- 必須完成 Google Cloud Partner Network 加入、簽署 Marketplace Vendor Agreement，並透過 Dynamic Client Registration (DCR) 實現 OAuth 2.0 認證
- 代理發布流程包括：在 Marketplace 設定定價和可用性、完成 Google Cloud 審查、透過 Procurement Flow 進行採購、透過 Registration Flow 完成註冊，最後由終端用戶在 Gemini Enterprise 中啟用

## 結論
透過遵循 A2A 協議標準和完成完整的市場整合流程，開發者可以將高品質 AI 代理發布到 Google Cloud Marketplace，讓企業用戶在 Gemini Enterprise 中安全地發現、採購和使用這些代理，實現 AI 代理的商業化。

---
