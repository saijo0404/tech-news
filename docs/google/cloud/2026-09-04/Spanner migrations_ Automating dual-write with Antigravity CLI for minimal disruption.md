# Spanner migrations: Automating dual-write with Antigravity CLI for minimal disruption

- **來源**: Google Cloud Blog Developers & Practitioners
- **發布日期**: 2026-09-05
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/using-antigravity-cli-to-streamline-dual-write-database-migration/

## 核心主題
Google 金融工程團隊使用 Antigravity CLI 自動化雙寫遷移，實現最小化中斷的數據庫遷移。

## 關鍵重點
- 使用標準化 MutationConverter 介面隔離數據庫遷移邏輯，使 AI 代碼代理能可靠生成代碼
- 採用頭部模式自動化跨多個 DAO 的代碼遷移，支持批量執行和自動驗證
- 結合測試系統確保數據一致性和代碼質量，大幅降低遷移成本

## 結論
這種方法讓工程師能專注於數據建模、架構韌性和性能優化等高價值工作，同時保持高數據忠實度。

---
