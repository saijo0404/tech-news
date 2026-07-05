# How I learned Go in a Day with Antigravity 2.0 and How You Can Do the Same

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-16
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/how-i-learned-go-in-a-day-with-antigravity-20-and-how-you-can-do-the-same/

## 核心主題
Google Cloud 開發者 Alex Astrum 分享如何透過 AI 代理工具 Antigravity 2.0（內建 Gemini），在一天內將 TypeScript 專案 `npx skills` 完整移植為零依賴的 Go 二進位工具 `skl`，並反思這段旅程對開發者行為模式的深刻影響。

## 關鍵重點
- **系統化的 AI 輔助遷移流程**：從技術選型（比較 Rust、Python、Zig、Swift 後選擇 Go）、安裝社群 Go Agent Skill（samber/cc-skills-golang），到透過明確的架構目標驅動 AI 完成差距分析、TDD 測試驅動開發、平行子代理協作，以及「大象與金魚」上下文管理模式，最終產出啟動僅 2ms、記憶體僅 11MB 的高效能工具。
- **品質保證與可重用的 Agent Skill**：單元測試通過並不夠，人類審查發現了安裝位置組合測試缺口；作者進一步建立了可重用的 `/cli-to-go-migration` Agent Skill，以五項核心規則（目標導向、設定驗證、匯入既有知識、斷點、對齊檢查）確保未來 Agent 行為與人類目標一致。
- **行為模式的深刻轉變**：離開 IDE 改用 Antigravity 2.0 迫使開發者保持「架構師」角色，從導航台指揮機器而非親自上手除錯。作者認為最深刻的收穫不是工具本身，而是學會如何大規模管理 Agent——信任 AI 的機械性工作，但對功能邏輯與測試覆蓋保持嚴格監督。

## 結論
重建 `skl` 不僅解決了個人工具需求，更是一段教育性旅程。作者強調「旅程本身就是回報」——透過將架構選擇編碼為可重用的 Skill，開發者得以成長。而操作無編輯器的 AI 代理工具，迫使開發者從「工程師」昇華為「架構師」，學會從高層次引導機器而非陷入細節，這正是大規模管理 Agent 的核心能力。

---
