# Don't just flag it, fix it: How to run CodeMender in your pull requests

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-11
- **原文連結**: https://cloud.google.com/blog/products/identity-security/how-to-run-codemender-in-your-pull-requests/

## 核心主題
Google 推出了 CodeMender，一個自動代碼安全代理，可以直接在 Git 拉取請求中發現並修復安全漏洞，無需開發人員離開工作流。

## 關鍵重點
- CodeMender 通過 /verify 和 /fix 命令，在拉取請求時間線內自動驗證漏洞並生成修復代碼
- 使用沙箱環境模擬漏洞利用，確保漏洞真實存在且可被利用
- 通過 GitHub Actions OIDC 令牌實現安全的身份驗證，避免長期憑證洩露
- 所有漏洞利用代碼在 Cloud Run 沙箱中運行，確保隔離和安全性

## 結論
CodeMender 將代碼安全自動化整合到開發工作流中，通過機器速度發現和修復漏洞，同時保持高度的安全性。
---