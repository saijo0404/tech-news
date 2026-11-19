# Lessons from building Sashiko, an agentic code review system for Linux

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-19
- **原文連結**: https://cloud.google.com/blog/products/application-development/lessons-from-building-sashiko-an-agentic-code-review-system/

## 核心主題
Google 團隊開發了 Sashiko，一個基於 Gemini 的自動程式碼審查系統，用於 Linux 核心代碼審查，以解決 AI 生成代碼帶來的審查負擔問題。

## 關鍵重點
- Sashiko 採用分階段審查機制，將問題發現與驗證分開，並要求每個階段記錄排除的問題
- 系統運行超過 7 個月，每天完成約 1200 次審查，已成為 Linux 核心開發過程的重要部分
- 數據顯示，自 Sashiko 推出後，60 天內需要跟進修復的合併提交比例從 3.4% 降至 2.2%，下降了 35%
- 通過清潔審查的提交在 60 天內需要跟進修復的比例僅為 0.9%，低於歷史基準的三分之一
- 關鍵發現：基於基準測試的開發優於直覺、程式碼代理不擅長審查自己的代碼、開放源碼和社區共同開發有助於建立信任

## 結論
Sashiko 證明 AI 輔助代碼審查可以有效減少漏洞滲透，並成為開源項目中維護者信任的重要工具。
---