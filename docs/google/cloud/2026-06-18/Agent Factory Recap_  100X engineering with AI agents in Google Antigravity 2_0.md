---
# Agent Factory Recap: 100X engineering with AI agents in Google Antigravity 2.0

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-18
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/agent-factory-recap-100x-engineering-with-ai-agents-in-google-antigravity-20/

## 核心主題
Google 資深 AI 工程師 Rody Davis 分享在 Antigravity 2.0 平台上實踐「100X 工程」的策略——透過 Skills 壓縮上下文、Bonsai 式程式碼審查，以及多代理並行架構，將開發者從日常瑣事中解放，專注於高階架構設計。

## 關鍵重點
- **Skills 作為代理的「作弊小抄」**：Skills 是壓縮上下文的核心哲學——將特定設計系統或 API 文件提供給代理，使其更快更準確地執行任務，避免在龐大未整理文件中搜尋的延遲。Rody 撰寫 Go CLI 將網站解析為 Markdown，可安裝數百個 Skills 確保代理隨時存取特定版本文件。
- **Bonsai 式架構與程式碼審查**：將維護程式碼庫比喻為 bonsai 藝術——持續修剪以保持簡潔。倡導扁平架構（狀態、UI、資料嚴格分離），讓代理出錯時架構違反立即顯現。程式碼審查策略依任務而異：行銷網站關注視覺輸出，後端邏輯則深究 API 合約；最佳做法是由開發者撰寫第一個範例，讓代理「複製模式」。
- **多代理並行與解耦 IDE 生態**：Antigravity 2.0 從單一 IDE 演進為四支柱平台——桌面 Agent Manager、CLI、SDK 與專用 IDE，解耦設計讓 CLI 適合 SSH 遠端工作（如 Raspberry Pi），Agent Manager 處理跨資料夾知識工作。Live Demo 展示單一語音提示即可啟動平行子代理（含 DevOps 與 QA），用 Vite+Go+SQLite 建構多語筆記應用並同時本地化為五種語言。

## 結論
代理工程時代已來臨，但 Rody Davis 證明它需要更多架構紀律而非更少——將程式碼庫視為 bonsai、將代理視為交響樂團，開發者能跨越「瑣碎勞動」，專注建構未來框架。同時，Rody 警告糟糕的程式碼健康度才是 AI 開發速度的最大瓶頸，而非上下文視窗大小。

---
