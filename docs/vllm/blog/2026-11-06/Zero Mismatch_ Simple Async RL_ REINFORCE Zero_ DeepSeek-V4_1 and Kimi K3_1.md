# Zero Mismatch, Simple Async RL: REINFORCE Zero, DeepSeek-V4.1 and Kimi K3.1

- **來源**: vLLM Blog
- **發布日期**: 2026-11-06
- **原文連結**: https://vllm.ai/blog/2026-11-06-zero-mismatch-async-rl

## 核心主題
這篇文章介紹了 REINFORCE Zero 方法，通過對齊計算核（kernels）和未裁剪重要性採樣（unclipped IS），實現了穩定的異步強化學習，即使在政策延遲（policy lag）高達 64 的情況下也能有效學習。

## 關鍵重點
- 異步 RL 比同步 RL 更快，但存在權重延遲（weight lag）問題，因為訓練使用的是較舊權重產生的樣本。
- 異步 RL 存在兩個問題：權重延遲（平滑變化）和核不匹配（fluctuates）。標準重要性採樣（IS）只能處理權重延遲，無法解決核不匹配。
- REINFORCE Zero 方法通過對齊計算核（align kernels）消除核不匹配，然後使用未裁剪重要性採樣（unclipped IS）處理剩餘的權重延遲，無需樣本拒絕閘。
- 實驗結果顯示，REINFORCE Zero 可以穩定訓練 20,000 次更新，在政策延遲 64 的情況下仍能學習，且訓練步吞吐量比同步訓練高 2.40 倍。
- 該方法已成功應用於 DeepSeek-V4.1-Flash 和 Kimi K3.1 等旗艦模型，包括在 AMD MI355X 上。

## 結論
通過對齊計算核和未裁剪重要性採樣，REINFORCE Zero 方法成功解決了異步 RL 中的核不匹配問題，實現了穩定高效的訓練，為大模型訓練提供了新的方向。
---
