# Announcing Claude apps gateway for Google Cloud

- **來源**: Google Cloud Blog
- **發布日期**: 2026-07-02
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/announcing-claude-apps-gateway-for-google-cloud/

## 核心主題
Google Cloud 推出 Claude apps gateway，解決企業部署 Claude Code 時的治理與安全問題。

## 關鍵重點
- **身份驗證與權限管理**：通過 Google Workspace 或 OIDC 進行身份驗證，開發者無需管理敏感憑證，如服務帳戶金鑰或 API 金鑰
- **政策集中管理**：RBAC 規則集中管理於 gateway.yaml，可快速更新並應用到所有開發者，無需逐台更新 managed-settings.json
- **使用追蹤與預算控制**：每個 token 使用都經過驗證，支持每日/每週/每月支出限制，防止使用失控

## 結論
Claude apps gateway 為企業提供安全、可治理的 Claude Code 部署解決方案，簡化開發者管理流程，確保符合企業合規要求。

---