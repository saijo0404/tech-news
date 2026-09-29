# Agent Factory recap: Agent harnesses, shifting left, and autonomous coding

- **來源**: Google Cloud Blog Developers & Practitioners
- **發布日期**: 2026-09-25
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/agent-factory-recap-agent-harnesses-shifting-left-and-autonomous-coding/

## 核心主題
這篇文章透過 Agent Factory 訪談，探討如何構建自主代理（agents），重點介紹「agent harness」概念、左移（shifting left）工程實踐，以及如何利用工具而非自訂 harness 來提升代理效能。

## 關鍵重點
- **Agent Harness**：LLM 加上周圍環境（如 Google Antigravity），讓模型能查詢即時資料並與工作空間互動，解決單一模型無法處理複雜任務的問題
- **左移（Shifting Left）**：將工程最佳實踐（linters、測試、文件）提前到開發生命週期早期，作為自動化的防護機制，避免反覆調整提示
- **工具優先**：使用標準 CLI 工具和現有 harness（如 Google ADK），避免自訂複雜框架，專注於提升工具品質和上下文策展
- **自主編碼**：工程師不再撰寫個別程式碼行，而是透過自然語言規範和最終成果（如 pull request）來管理，專注於成果審查
- **代理團隊策展**：將團隊成員的專業知識整合到代理環境中，像 RPG 角色屬性一樣提升代理能力，實現多技能自主分類

## 結論
真正的開發者槓桿來自於將最佳實踐左移、投資豐富的工具和上下文，以及使用輕量級但高效的模型組合。當模型、harness 和知識庫三者協同運作時，代理才能從單純的對話工具轉變為可靠的自主工程夥伴。

---