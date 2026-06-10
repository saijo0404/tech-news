---
# Choosing your surface: Antigravity 2.0, Antigravity CLI, Antigravity IDE, or Antigravity SDK

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-10
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/choosing-your-surface-antigravity-20-antigravity-cli-antigravity-ide-or-antigravity-sdk/

## 核心主題
Google 介紹 Antigravity 2.0 的四種使用介面，讓開發者能根據自己的工作習慣與需求，選擇最適合的介面來使用 Antigravity AI 代理工具。

## 關鍵重點
- **Antigravity 2.0（桌面應用程式）**：預設推薦選項，可同時管理多個專案中的獨立任務，支援排程例行檢查（如程式碼品質審查或套件過時偵測）。
- **Antigravity CLI（終端機介面）**：以 Go 打造，適合偏好鍵盤操作與無頭環境（SSH、遠端容器）的開發者，可在背景啟動代理而不鎖定工作視窗。
- **Antegravity IDE（整合開發環境）**：將代理直接嵌入編輯器，讓開發者能逐行檢視、接受或拒絕代理的修改，並內建除錯功能讓代理自動修復執行期錯誤。
- **Antigravity SDK（Python 程式庫）**：讓開發者從頭建構自訂代理，共用與 Google 官方工具相同的底層工具與規則，可本地開發後零修改部署至 Google Cloud。

## 結論
四種介面雖然外觀與使用場景不同，但都建立在相同的 Agent Harness 之上，支援外掛（plugins）、技能（skills）等核心功能；開發者可依需求挑選最適合的路徑，輕鬆進入 Antigravity 生態系。

---
