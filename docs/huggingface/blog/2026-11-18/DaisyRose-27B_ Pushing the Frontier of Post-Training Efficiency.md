# DaisyRose-27B: Pushing the Frontier of Post-Training Efficiency

- **來源**: Hugging Face
- **發布日期**: 2026-11-18
- **原文連結**: https://huggingface.co/blog/RadixArk/daisyrose-27b-pushing-the-frontier-of-post-trainin

## 核心主題
RadixArk 推出 DaisyRose-27B 模型，基於 Qwen3.8-27B 並使用 Miles 強化學習訓練，在後訓練效率上取得突破。

## 關鍵重點
- 在 Terminal-Bench 4.1 測試中，通過率從 5.6% 提升至 12.0%，在所有基準測試中均優於原始 Qwen3.8-27B 模型
- 使用 144 台 H200 GPU 在 18 天內訓練，僅使用 1,200 個精選任務，訓練成本降低 57%，速度提升 2 倍
- 模型保留 Qwen3.8-27B 的架構、分詞器、聊天模板、圖像理解和 256K token 上下文窗口，可通過 SGLang 和 DSpark 推理服務

## 結論
DaisyRose-27B 展示了後訓練效率的顯著提升，為大模型訓練提供了更具成本效益和效率的解決方案，模型已開放下載並可通過 Miles 框架自訓。
---
