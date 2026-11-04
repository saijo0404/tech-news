# CWE-bench v2: More coverage, quality, and transparency

- **來源**: Hugging Face
- **發布日期**: 2026-11-03
- **原文連結**: https://huggingface.co/blog/cwe-bench

## 核心主題
CWE-bench v2 是一個公開的100個任務集合，用於測試前沿AI模型在發現和修復安全漏洞方面的能力，涵蓋91種不同的CWE漏洞類型。

## 關鍵重點
- 100個任務涵蓋91種不同的CWE漏洞類型，測試模型在發現和修復安全漏洞方面的能力
- 所有任務都經過嚴格審查，確保指令真實、評分標準公平，並由LLM評審小組協助設計
- 結果完全程序化，任何人都可以重複驗證，並有保留集用於追蹤未見過的任務進度
- Gemini 4 Argon以67.8%的pass@1率領先，但即使領先者仍會失敗19%的任務
- 任務可以通過Hugging Face Hub直接運行，使用Harbor框架，並標記為rl-environment可用於訓練防禦性代理

## 結論
CWE-bench v2公開了數據集、評分器和工具集，歡迎社區反饋和貢獻，鼓勵人們運行自己的模型並分享結果。
---
