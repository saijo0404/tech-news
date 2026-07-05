# Choosing your surface: Antigravity 2.0, Antigravity CLI, Antigravity IDE, or Antigravity SDK

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-10
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/choosing-your-surface-antigravity-20-antigravity-cli-antigravity-ide-or-antigravity-sdk/

## 核心主題
Google 介紹 Antigravity 2.0 生態系中的四種開發介面——桌面應用、命令列工具、IDE 整合與 Python SDK，讓開發者依工作流程選擇最適合的 Agent 使用方式，所有介面共享同一底層 Agent 框架。

## 關鍵重點
- **Antigravity 2.0 桌面應用**：預設推薦介面，可同時管理多個專案的平行 Agent 任務，支援排程任務（如定期檢查程式碼品質或過時套件），從單一螢幕輕鬆切換與監控不同專案。
- **Antigravity CLI 與 IDE**：CLI 以 Go 開發，提供快速的命令列鍵盤操作與背景 Agent 執行，適合 SSH 連線或遠端容器等非互動式場景；IDE 介面則讓 Agent 直接在開發者工作空間中編輯程式碼，支援逐行接受或拒絕變更，並內建除錯功能讓 Agent 能看到執行階段錯誤並一鍵修復。
- **Antigravity SDK（Python）**：提供 Python 函式庫，開發者可從頭建立自訂 Agent 並部署至 Google Cloud；SDK 運行於相同的共享框架上，享有與 Google 官方工具相同的工具與規則支援，並相容外掛（plugins）與技能（skills）系統。

## 結論
無論選擇哪種介面，所有 Antigravity 表面都運行在同一底層 Agent 框架上，共享相同的工具、外掛與技能生態系；開發者可依據工作需求——從平行任務管理、命令列自動化、直接在 IDE 中協同編碼，到建構客製化 Agent 管線——靈活選擇最適合的介面。

---
