# Accelerating Gemini Nano models on Pixel with frozen Multi-Token Prediction

- **來源**: Google Research Blog
- **發布日期**: 2026-06-26
- **原文連結**: https://research.google/blog/accelerating-gemini-nano-models-on-pixel-with-frozen-multi-token-prediction/

## 核心主題
Google 提出「凍結式多詞元預測」（Frozen MTP）架構，將 Multi-Token Prediction 技術適配至已部署的 Pixel 裝置上，透過凍結主模型權重並附加輕量 MTP 頭部，在不影響生成品質與安全對齊的前提下，為 Pixel 9 與 10 系列帶來 50% 以上的推理加速與顯著節能效果。

## 關鍵重點
- **凍結主體幹的 MTP 架構**：MTP 取代傳統的獨立草稿模型（如 EAGLE 架構），改為在已訓練好的 Gemini Nano v3 主模型最終層附加一個輕量 Transformer 頭部。主模型權重完全凍結，僅訓練 MTP 頭的參數以最小化未來詞元的預測誤差。由於錯誤草稿在驗證階段會被捨棄，最終輸出與主模型逐位元相同，確保完全向後相容且無效能退化。
- **零複製架構節省記憶體**：傳統 MTP 實作與主模型共享靜態參數，但草稿模型仍需維護自己的 KV cache，在行動裝置上造成記憶體「雙重稅」。Google 設計零複製架構，讓 MTP 頭部直接跨注意力（cross-attend）至主模型凍結的 KV cache，無需自行維護歷史上下文。這消除了草稿模型的預填延遲，並每台裝置節省約 130MB 動態記憶體（含草稿詞元嵌入查找表、預填點注意力變體等）。
- ** richer 表示帶來實質加速**：MTP 頭部直接取得主模型最終高維激活值（hidden states），比獨立草稿模型僅基於文字歷史預測更精準。在 Pixel 9 裝置上，MTP 相較於同等參數的獨立草稿模型加速 50% 以上；在結構可預測任務（如智慧回覆）中詞元接受率提升高達 55%。在生產負載（AI 通知摘要、校對）中，每輪推理平均正確預測多近兩個詞元，減少驗證步驟也降低重處理器喚醒時間、改善電池續航。

## 結論
凍結式 MTP 為邊緣運算環境下的 LLM 加速提供了創新途徑——不需重新訓練或微調獨立草稿模型，即可將多詞元預測的效率增益部署至現有裝置。這項技術已推出至 Pixel 9 與 10 系列，讓通知摘要與校對等功能更快、更省電。未來 Google 將探索平行解碼、分支可能性探索與驗證寬鬆等方向，進一步突破行動裝置上 AI 生成的效能極限。

---
