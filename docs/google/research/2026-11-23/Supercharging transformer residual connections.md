# Supercharging transformer residual connections

- **來源**: Google Research Blog
- **發布日期**: 2026-11-23
- **原文連結**: https://research.google/blog/supercharging-transformer-residual-connections/

## 核心主題
本文介紹了 DeepCrossAttention (DCA) 架構，透過使用可學習權重和深度跨注意力機制來動態組合先前層次的輸出，從而解決傳統殘差連接中的資訊稀釋問題。

## 關鍵重點
- DCA 將殘差學習重新定義為動態路由問題，允許每個層根據特定 token 動態選擇和組合先前層的嵌入
- 相比傳統殘差連接，DCA 可減少 30-40% 的參數數量，同時保持或提升學習效果
- 在 LM1B 數據集上，DCA 模型只需 30 層即可達到標準 Transformer 42 層的表現，實現 29% 的深度和參數減少
- 參數增加量僅佔總模型大小的 0.2% 以下，計算和記憶體佔用可忽略
- 實驗顯示 DCA 在語言建模、圖像分類等多個任務中均展現出更快的收敛速度和更穩定的訓練

## 結論
從靜態殘差連接轉向動態、基於注意力的路由是構建更高效模型的強大策略。未來模型將根據特定 token 動態權重和路由過去層的表示，實現所有模型層作為專業協作，最大化資訊共享且無冗餘。

---