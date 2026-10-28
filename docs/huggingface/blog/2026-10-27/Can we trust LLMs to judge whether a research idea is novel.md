# Can we trust LLMs to judge whether a research idea is novel?

- **來源**: Hugging Face
- **發布日期**: 2026-10-27
- **原文連結**: https://huggingface.co/blog/allenai/novelty-bench

## 核心主題
研究顯示，大型語言模型在評估科學研究想法的新穎性方面並不可靠，特別是對於 AI 生成的想法，提示詞的小變化會導致判斷結果大幅波動。

## 關鍵重點
- 研究團隊建立了「Old Ideas, Novel Problems」基准，測試了六個 LLM 判斷者（GPT-5.1/5.2/5.4 和 Claude Sonnet/Opus 4.5/4.6）在評估研究想法新穎性方面的可靠性
- 提示詞的小變化會導致判斷準確度相差超過 50 個百分點，顯示判斷極度敏感
- 在 AI 生成的想法上，判斷特別脆弱；在人類撰寫的研究上相對穩定，但並非完全免疫
- 更複雜的搜尋和推理並未一致改善判斷，簡單的提示反而更有效且成本更低
- 目的導向的評估系統（如 Idea Novelty Checker 和 Sakana AI's AI Scientist）比簡單提示的 Claude Opus 4.6 基準表現更差且昂貴

## 結論
LLM 基於的新穎性評估仍是重大未解決問題，需要更多可靠的方法來判斷 AI 是否真的提出了新想法。研究團隊提供了基准、數據和代碼，幫助研究者建立更可靠的評估方式。

---