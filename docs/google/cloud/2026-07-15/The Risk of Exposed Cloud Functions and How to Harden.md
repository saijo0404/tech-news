# The Risk of Exposed Cloud Functions and How to Harden

- **來源**: Google Cloud Blog Threat Intelligence
- **發布日期**: 2026-07-16
- **原文連結**: https://cloud.google.com/blog/topics/threat-intelligence/exposed-cloud-functions-harden/

## 核心主題
這篇文章探討了公開暴露的雲端函式（serverless applications）的安全風險，並提供具體的加固建議。

## 關鍵重點
- 公開暴露的雲端函式可能缺乏身份驗證，易受 LFI/RFI、命令注入等攻擊，攻擊者可能獲取完整容器控制權限
- 常見攻擊手法包括提取代碼中的密鑰、利用未驗證的用戶輸入進行文件包含、通過 shell 執行提取服務帳戶憑證
- 加固建議包括：實施安全軟體開發生命週期（S-SDLC）、使用隔離的服務專案、採用最小權限 IAM、部署 Layer 7 負載平衡器與 Cloud Armor WAF

## 結論
雖然「vibe-coding」提升了開發效率，但企業必須將安全整合到開發生命週期早期，採用防禦深度策略，並優先關注身份驗證與架構設計。

---