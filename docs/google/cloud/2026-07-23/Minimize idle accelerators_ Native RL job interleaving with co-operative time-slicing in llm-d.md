# Minimize idle accelerators: Native RL job interleaving with co-operative time-slicing in llm-d

- **來源**: Google Cloud Blog
- **發布日期**: 2026-07-24
- **原文連結**: https://cloud.google.com/blog/products/containers-kubernetes/introducing-co-operative-time-slicing-for-rl-in-llm-d/

## 核心主題
Google 推出 llm-d 平台的合作時間切片技術，透過將 RL 任務視為可動態調度的實體，將獨立 RL 任務交錯到共享硬體上，大幅提升加速器的利用率。

## 關鍵重點
- 將 RL 的離散步驟（如採樣 rollout 和梯度訓練）視為動態可調度的實體
- 同步設定中，平台交錯訓練器和採樣器以最小化交替閒置窗口
- 非同步工作負載利用時間切片動態回收和利用 RL 訓練器迭代之間的碎片閒置時間
- 初始基準測試顯示，此平台級多工化將加速器任務週期從 ~40% 基線提升至 70%，且未影響模型收敛或準確性
- 透過消除累積的浪費計算，顯著改善價格性能和降低總擁有成本

## 結論
此技術透過消除因同步階段等待造成的 GPU 閒置時間，大幅降低 RL 訓練的 TCO，同時保持模型準確性。
---
