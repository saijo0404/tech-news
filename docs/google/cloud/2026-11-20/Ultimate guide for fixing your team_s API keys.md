# How to fix your team's API keys

- **來源**: Google Cloud Blog Developers & Practitioners
- **發布日期**: 2026-11-21
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/how-to-fix-your-teams-api-keys/

## 核心主題
這篇文章提供完整的指南，幫助團隊從使用原始 API Key 轉向使用身份驗證（Identity-based Authentication）系統，以解決 API Key 洩露風險和團隊協作問題。

## 關鍵重點
- **使用 Application Default Credentials (ADC)**：讓每位團隊成員使用單一登入方式呼叫 Gemini、Claude 等模型，取代直接複製 API Key。
- **為應用程式建立專屬服務帳號**：將應用程式與開發者個人身份分離，限制權限範圍，降低洩露風險。
- **將剩餘 API Key 移至 Secret Manager**：所有第三方服務（如 Stripe、Slack）的 Key 應儲存在 Secret Manager，而非.env 檔案或聊天軟體中。
- **實施權限控制與預算管制**：授予最小必要權限（roles/aiplatform.user），並設定支出上限（Spend Cap）以控制成本。
- **使用掃描工具與刪除舊 Key**：掃描專案尋找洩露的 Key，並徹底刪除所有 AI Studio API Key。

## 結論
透過將團隊和應用程式都建立在身份驗證基礎之上，不僅能消除 API Key 洩露風險，還能獲得預算管制、提示防護、代碼沙盒等多層安全防護。這套方案在保持原型開發速度的同時，大幅提升生產環境的安全性。

---