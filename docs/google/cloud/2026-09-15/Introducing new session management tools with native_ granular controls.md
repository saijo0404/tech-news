# Introducing new session management tools with native, granular controls

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-16
- **原文連結**: https://cloud.google.com/blog/products/identity-security/introducing-new-session-management-tools-with-native-granular-controls/

## 核心主題
Google Cloud 推出了新的會話管理工具，將會話控制從廣泛的管理設置演變為 Context-Aware Access (CAA) 的細粒度功能，提供更高的靈活性、更好的自動化以及更自然的保安工作流程。

## 關鍵重點
- **自動化優先**：支援 Terraform、gcloud CLI 和 REST API，讓使用者可以程式化地定義、部署和管理會策政策，支援 DevSecOps 工作流
- **精確的目標設定**：使用 Google Groups 取代組織單位 (OUs)，允許針對特定用戶群組（如高權限管理員）應用不同的會策政策
- **精確的應用控制**：可以針對特定應用（如 Google Cloud Console、gcloud 工具、特定 OAuth 應用）配置會策控制，避免一刀切政策造成的不必要干擾
- **Google Cloud 原生體驗**：允許在 Google Cloud Console 中管理會策政策，提供統一的體驗，讓偏好使用 Google Console 的管理員擁有更大的靈活性

## 結論
透過將靜態的組織預設值演變為動態的、情境感知的政策，安全團隊可以在風險最高的地方實施更嚴格的重新驗證邊界，同時不會影響開發者的速度。

---