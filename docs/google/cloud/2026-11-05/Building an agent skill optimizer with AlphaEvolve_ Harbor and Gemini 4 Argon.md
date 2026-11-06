# Building an agent skill optimizer with AlphaEvolve, Harbor and Gemini 4 Argon

- **來源**: Google Cloud Blog Developers & Practitioners
- **發布日期**: 2026-11-06
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/how-to-build-an-agent-skill-optimizer-with-alphaevolve-and-harbor/

## 核心主題
這篇文章介紹了如何使用 AlphaEvolve、Harbor 和 Gemini 4 Argon 構建一個代理技能優化器，以自動改進 AI 代理的技能，使其在執行任務時更有效率。

## 關鍵重點
- AlphaEvolve 將技能視為程式碼，讓 Gemini 自動優化技能描述和指令，類似於程式碼優化流程
- Harbor 作為評估器，在真實任務上運行代理並提供評分和反饋，形成完整的優化循環
- 通過並行測試確保評分可信，將每個候選技能與基準技能在同一任務上同時運行以消除噪音
- 實驗顯示優化後的技能能將成功率提升 5%，特別是在處理代理常見的失敗模式（如時間限制）上效果顯著

## 結論
這種自動化優化方法比手寫技能更有效，特別適合解決代理常見的失敗模式。未來將進一步測試 AlphaEvolve 在企業代理框架（系統提示、政策指令和工具）上的應用，以處理代理缺乏的業務規則。

---