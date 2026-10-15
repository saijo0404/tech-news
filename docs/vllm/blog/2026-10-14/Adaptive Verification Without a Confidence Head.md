# Adaptive Verification Without a Confidence Head

- **來源**: vLLM Blog
- **發布日期**: 2026-10-14
- **原文連結**: https://vllm.ai/blog/2026-10-14-adaptive-verification-online-estimator

## 核心主題
vLLM 現在支持所有基於草稿模型的預測器類型進行置信度評分，即使沒有置信頭，也能使用線上適配估計器來預測目標模型接受草稿的概率。

## 關鍵重點
- **無需重新訓練**：對於缺乏置信頭的草稿模型（如 EAGLE、MTP、DFlash），新增輕量邏輯迴歸估計器，可從草稿模型的 logit 中推導出接受概率，無需重新訓練草稿模型。
- **線上適配係數**：估計器的係數（斜率與截距）在服務期間持續根據目標模型的接受/拒絕決策進行適配，能適應不同工作負載和模型組合。
- **logit(q_max) 特徵選擇**：經過多項評估指標（AUC、log-loss、ECE 等），最終選擇 logit(q_max) 作為特徵，在保持無偏性（losslessness）的同時，在 AUC 和 ECE 上取得良好平衡。
- **相比訓練的置信頭表現更優**：在 DeepSeek-V4-Flash + DSpark 組合上，線上估計器在 AUC 上比訓練的置信頭高出 0.0146，且在後續位置（第 2 位以後）優勢更明顯。

## 結論
這項功能大幅擴展了適配性驗證（Adaptive Verification）的適用範圍，讓更多現有的草稿模型無需重新訓練即可受益於性能優化，同時提供了比傳統訓練置信頭更好的接受概率估計表現。
---