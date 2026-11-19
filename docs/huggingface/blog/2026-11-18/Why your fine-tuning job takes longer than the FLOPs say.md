# Why your fine-tuning job takes longer than the FLOPs say

- **來源**: Hugging Face Blog
- **發布日期**: 2026-11-18
- **原文連結**: https://huggingface.co/blog/Dharma-AI/predicting-fine-tuning-time

## 核心主題
Dharma-AI 團隊通過分析 272 個真實的 supervised fine-tuning (SFT) 任務，發現傳統的 FLOP 計算方法無法準確預測 GPU 集群上的精調時間，並提出了一個基於 CatBoost 的預測模型，將平均絕對誤差從 12.41 小時降低到 1.71 小時。

## 關鍵重點
- 傳統 FLOP 計算方法無法準確預測實際精調時間，因為它只考慮計算量而忽略了環境設置、模型下載、檢查點上傳等額外開銷
- Dharma-AI 團隊分析了 272 個真實任務，發現 CatBoost 預測模型在 5 折交叉驗證中達到 R² = 0.98，平均絕對誤差僅為 1.71 小時
- 預測模型最重要的特徵包括評估數據量 (num_eval_data)、可訓練參數數量 (num_trainable_params) 和檢查點數量 (num_params_saved)

## 結論
使用基於歷史運行數據的机器学习模型（如 CatBoost）來預測精調時間，比傳統的 FLOP 計算方法準確得多，可以幫助集群調度器更好地規劃 GPU 資源分配。
---