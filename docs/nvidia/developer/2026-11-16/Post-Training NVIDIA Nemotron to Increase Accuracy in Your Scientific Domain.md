# Post-Training NVIDIA Nemotron to Increase Accuracy in Your Scientific Domain

- **來源**: developer.nvidia.com/blog
- **發布日期**: 2026-11-16
- **原文連結**: https://developer.nvidia.com/blog/post-training-nemotron-to-increase-accuracy-in-your-scientific-domain/

## 核心主題
這篇文章介紹了如何使用 NVIDIA Nemotron 3.5 Super VL 模型透過後訓練（特別是強化學習）來提升科學領域任務的準確性。

## 關鍵重點
- 使用 NeMo Gym 建構強化學習環境，從實驗數據（如 MetxBioDB）訓練模型
- 採用 GRPO + LoRA 微調，並使用 RLVR 架構進行驗證
- 可選精煉：使用強教師模型（如 Claude Sonnet 5.5）生成高品質推理軌跡作為暖啟動
- 實例成果：藥物代謝預測任務中，RL 後訓練再提升 17% 準確度

## 結論
此流程可複製到其他科學領域，只需替換環境配置與驗證工具。