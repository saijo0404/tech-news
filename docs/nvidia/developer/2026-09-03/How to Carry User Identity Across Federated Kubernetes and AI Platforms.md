# How to Carry User Identity Across Federated Kubernetes and AI Platforms

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-09-03
- **原文連結**: https://developer.nvidia.com/blog/how-to-carry-user-identity-across-federated-kubernetes-and-ai-platforms/

## 核心主題
本文介紹了如何在分散式 Kubernetes 和 AI 平台中，透過中央身份閘門模式來統一傳遞使用者身份驗證狀態，解決傳統 SSO 無法將身份驗證狀態傳遞到分散數據平面的問題。

## 關鍵重點
- **中央身份閘門模式優勢**：NVIDIA 內部平台減少 55% 重複登入，提供統一平台體驗、統一登出、降低上層負載，並標準化身份標頭。
- **技術架構**：使用中央身份閘門管理 OIDC 流程、區域閘門執行權限控制、共享會話儲存（Redis）以及 mTLS 等安全防護。
- **實施步驟**：先清查現有會話創建位置、定義中央合約、逐步遷移，從單一區域閘道開始，保持應用程式介面穩定。
- **AI 助手受益**：統一身份驗證讓 AI 助手能透過平台會話驗證使用者身份，無需個別工具認證，可繼承使用者 RBAC 權限。

## 結論
透過中央身份閘門模式，平台能大幅減少重複登入事件並提供一致的使用者體驗，為統一開發者門戶與 AI 助手奠定基礎，使平台能支援更多工具與工作流。

---