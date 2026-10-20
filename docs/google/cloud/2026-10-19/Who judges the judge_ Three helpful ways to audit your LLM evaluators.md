# Who judges the judge? Three helpful ways to audit your LLM evaluators

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-20
- **原文連結**: https://cloud.google.com/blog/topics/consulting/three-ways-to-audit-your-llm-evaluators/

## 核心主題
這篇文章探討了 LLM 評估者（作為法官的 LLM）的偏見問題，並提出了三個支柱方法來審計和改進 LLM 評估器的質量。

## 關鍵重點
- LLM 評估者存在多種偏見（如 verbosity bias、position bias、halo effect 等），並非客觀的真理仲裁者，而是帶有自身偏見的模型
- 三個審計支柱：測量內部穩定性（測試一致性）、驗證人類對齊（使用機會校正指標）、使用多評估器集成（分解提示與多模型集成）
- 企業需要採用統計審計的評估管道，以確保 LLM 評估器的質量，避免工作受到損害

## 結論
LLM 評估器並非完美的客觀工具，需要通過系統化的審計方法（內部穩定性、人類對齊、多評估器集成）來提升其質量，否則可能導致評估結果失真。

---