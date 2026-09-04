# Training a coding model to paint watercolours with TRL and OpenEnv

- **來源**: Hugging Face Blog
- **發布日期**: 2026-09-03
- **原文連結**: https://huggingface.co/blog/train-to-paint-with-code

## 核心主題
這篇文章介紹了一個使用語言模型訓練出能繪製水彩畫的程式碼模型實驗，使用 TRL 和 OpenEnv 框架，透過 RLHF 機制優化模型審美偏好。

## 關鍵重點
- 模型生成約 150 行 JavaScript 程式碼，使用 10 種繪畫方法模擬兒童畫筆觸
- 訓練平台使用 Hugging Face Jobs + Spaces，獎勵機制包含程式碼編譯、長度、兩兩比較和 HPSv3 審美評分
- 建立 178 幅手動評分的水彩畫作池作為參考基準，訓練三組實驗比較不同獎勵權重分配
- 三組實驗均成功學習，judge-led 獎勵提升最顯著 (+0.27)，證明 RL over taste 可行
- 技術調整包括 LoRA 參數調整、學習率調整和 GRPO scheduler 調整
- 基礎設施挑戰包括 trainer、Spaces、inference router 和 websocket 協同運作，故障率約 1.5%-5.2%
- 未來方向包括多步驟訓練、嘗試更小模型和改進參考池構建

## 結論
這個實驗成功證明了使用語言模型訓練程式碼模型來繪製藝術作品的可行性，並提供了可重現的開放源碼解決方案。

---