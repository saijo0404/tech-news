# The sleep framework: A new way for LLMs to retain knowledge in continual learning

- **來源**: Google Research Blog
- **發布日期**: 2026-10-27
- **原文連結**: https://research.google/blog/the-sleep-framework-a-new-way-for-llms-to-retain-knowledge-in-continual-learning/

## 核心主題
本文介紹了一種名為「睡眠框架」的持續學習方法，讓大型語言模型（LLM）能像人類大腦一樣，在活躍學習與離線記憶整合之間交替，從而持續學習新知識而不遺忘舊知識。

## 關鍵重點
- **記憶整合階段**：通過混合專家（MoE）架構和知識種子技術，將短期記憶整合到長期參數中，防止災難性遺忘
- **夢境階段**：模型自主生成合成訓練數據並進行強化學習優化，探索不同知識領域並提升推理能力
- **實證效果**：在長上下文理解（10M tokens）、持續翻譯和數學推理等任務上，表現優於傳統方法

## 結論
睡眠框架為自主持續學習的 AI 系統提供了新途徑，通過交替活躍學習與離線休息，使 LLM 能保留短期記憶、抽象新技能到長期參數結構，並持續自我改進而不遺忘既有能力。

---