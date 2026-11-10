# Your Experts Have Partners. There's HOPE for Keeping Them Together

- **來源**: Hugging Face
- **發布日期**: 2026-11-09
- **原文連結**: https://huggingface.co/blog/amazon/higher-order-pruning-experts

## 核心主題
這篇文章介紹了 HOPE（Higher-Order Pruning of Experts）方法，一種用於混合專家（MoE）語言模型的專家剪枝技術，通過考慮專家之間的協同關係來優化剪枝決策。

## 關鍵重點
- 傳統的第一階剪枝方法只獨立評估每個專家的貢獻，忽略了專家之間的協同關係，導致剪枝效果不佳
- HOPE 是一種第二階剪枝方法，通過分析專家對之間的交互來優化剪枝決策，在 50% 剪枝率下比次佳方法高出 6.1%
- HOPE 方法通過考慮專家協同關係，在保持模型性能的同時實現了更有效的剪枝，特別適合高剪枝率場景

## 結論
HOPE 方法通過考慮專家協同關係，在保持模型性能的同時實現了更有效的剪枝，特別適合高剪枝率場景。

---