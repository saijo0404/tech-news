# Staying Ahead of Adversarial AI Through Agentic Source Code Review

- **來源**: Google Cloud Blog
- **發布日期**: 2026-08-18
- **原文連結**: https://cloud.google.com/blog/topics/threat-intelligence/staying-ahead-of-adversarial-ai-through-agentic-source-code-review/

## 核心主題
Google 發布內部工具 **Agentic Vulnerability Discovery Harness (AVDH)**，透過多代理協同分析代碼，大幅提升漏洞發現效率。

## 關鍵重點
- **主要成果**：10 個月內發現超過 100 個真實漏洞，包含 12 個分配 CVE（如 CVE-2026-13242、CVE-2026-55803），在 2 天內完成通常需更長時間的手動審查
- **系統架構**：使用 Google Agent Development Kit (ADK) 框架，採用 Google Antigravity 集中式工作空間管理，採用瀑布式流程
- **六大核心流程**：威脅建模 → 入口點發現 → 上下文豐富化 → 假設生成 → 假設驗證 → 專家驗證
- **關鍵優勢**：提高準確性與速度、減少假陽性、可與 CodeMender 掃描器結合形成雙層防禦、可應用於紅隊操作、滲透測試及事件響應
- **AI 定位**：AI 應作為人類專業知識的倍增器，而非替代，建議採用雙層防禦策略

## 結論
AVDH 透過多代理協同與專家知識注入，大幅加速漏洞發現流程，協助防禦者比攻擊者更快定位安全漏洞。建議結合 AVDH 的深入分析與 CodeMender 的持續監控，形成完整的雙層防禦體系。
---