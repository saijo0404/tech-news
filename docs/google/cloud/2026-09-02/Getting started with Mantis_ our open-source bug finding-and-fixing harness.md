# Getting started with Mantis, our open-source bug finding-and-fixing harness

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-03
- **原文連結**: https://cloud.google.com/blog/products/identity-security/getting-started-with-the-mantis-harness-to-find-and-fix-bugs/

## 核心主題
Google 推出 Mantis 開源框架，自動化發現、分類、重現和修復軟體漏洞，以應對 AI 模型在安全漏洞發現方面的能力。

## 關鍵重點
- Mantis 結合了評審員和審查員等行業標準代理技術，並使用沙盒重現漏洞來驗證，從而提高了準確性。
- 它分析倉庫歷史，從過去的修復中學習，並自動建立架構和威脅模型文檔，即使這些文檔未提供。
- 構建了分層安全摘要樹，將單一文件壓縮為目錄和根級別摘要，將 token 超載減少超過 85%，同時保留大型倉庫的關鍵結構上下文。
- 提供簡單的開始方式：克隆 Mantis 倉庫，然後使用特定提示語在編碼代理中啟動它。
- 推薦兩項實踐：為工具提供正確的上下文（例如，避免修復會導致用戶程序崩潰的錯誤），以及建立具有漏洞接受標準的網絡沙盒。

## 結論
Mantis 是開始利用 AI 驅動漏洞發現和現代化開發實踐的理想起點，特別適合希望提高漏洞發現準確性和修復效率的開發者。
---