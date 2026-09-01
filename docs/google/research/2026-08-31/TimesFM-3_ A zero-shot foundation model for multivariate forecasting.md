# TimesFM-3: A zero-shot foundation model for multivariate forecasting

- **來源**: Google Research Blog
- **發布日期**: 2026-08-31
- **原文連結**: https://research.google/blog/timesfm-3-a-zero-shot-foundation-model-for-multivariate-forecasting/

## 核心主題
TimesFM-3 是 Google Research 推出的新一代時間序列基礎模型，支援多變量預測，可同時預測多個相關時間序列並整合歷史與未來已知特徵，在多個公開評估基準上達到最優表現。

## 關鍵重點
- **多變量預測能力**：可同時預測多個相關時間序列（如不同冰淇淋品牌），支援點估計和分位數預測，無需任務特定微調
- **整合過去與未來特徵**：能納入僅知歷史的變數（如過去人流）和已知未來的變數（如促銷活動、天氣預報），提升預測準確度
- **單一前向傳播效率**：採用非自迴歸解碼策略，在單一前向傳播中完成整個預測時長，避免逐點預測的延遲和累積錯誤
- **頂尖基準表現**：在 Gift-Eval、FEV-Bench 和 Time 三個公開評估基準上，點估計和概率預測指標均取得最佳排名

## 結論
TimesFM-3 擁有 3.3 億參數，已在 GitHub 和 Hugging Face 開放，並預計近期推出 BigQuery 整合。此模型顯著提升了時間序列預測的準確性和效率，特別適合需要整合多變量資訊的實際應用場景。

---