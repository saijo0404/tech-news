# Changing the game: Using agentic AI to secure infrastructure code

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-19
- **原文連結**: https://cloud.google.com/blog/topics/systems/using-ai-agents-to-secure-google-infrastructure/

## 核心主題
Google 利用 AI 原生代理方法，將高精度的漏洞掃描和修復直接嵌入到軟體開發生命週期中，以防止漏洞進入代碼庫或生產環境。

## 關鍵重點
- 採用預提交代理掃描，將安全檢查整合到開發者日常使用的工具中，實現持續的安全檢查
- 使用本地化威脅模型，通過代碼庫元數據和依賴關係圖提高掃描準確性，將假陽率降至 3%
- 使用專業分發代理和後提交掃描，在低延遲情況下快速驗證漏洞，並通過 nightly 集成測試提供第二層防護
- 自動化修復代理使用掃描結果和生成的證明，自動構建符合內部編碼標準的修復方案

## 結論
這種將持續掃描直接嵌入軟體開發生命週期的方法已成為 Google 的遊戲改變者，任何組織都可以採用類似的 AI 原生方法來提高安全性。
---