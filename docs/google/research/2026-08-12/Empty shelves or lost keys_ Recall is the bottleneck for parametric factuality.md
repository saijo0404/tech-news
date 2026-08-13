# Empty shelves or lost keys? Recall is the bottleneck for parametric factuality

- **來源**: Google Research Blog
- **發布日期**: 2026-08-12
- **原文連結**: https://research.google/blog/empty-shelves-or-lost-keys-recall-is-the-bottleneck-for-parametric-factuality/

## 核心主題
研究團隊開發了「知識 profiling」框架，發現 frontier LLMs 的錯誤主要來自於 recall failure（遺失的鑰匙），而非 encoding failure（空書架）。

## 關鍵重點
- 引入了 WikiProfile 基準測試，包含 2,150 個維基導出的事實，每個事實搭配 10 個問題來測試 encoding、recall 和 recognition。
- 發現 frontier LLMs（如 Gemini-3 和 GPT-5）的 95-98% 事實已被編碼，但仍無法直接回憶 26-34% 的事實。
- 思考（thinking）可以恢復 40-65% 已編碼但無法直接回憶的事實，顯示思考是 recall 的輔助機制。
- 稀有事實的編碼率與流行事實相近，但 recall 差距更大，顯示 bottleneck 從知識獲取轉向知識利用。
- 反向問題在生成任務中較直接問題困難，這是一種 recall 問題而非知識缺失。

## 結論
未來提升事實性應著重於知識利用而非單純擴大模型規模或數據覆蓋。

---