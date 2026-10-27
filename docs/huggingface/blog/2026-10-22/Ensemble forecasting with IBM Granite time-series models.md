# Ensemble forecasting with IBM Granite time-series models

- **來源**: Hugging Face
- **發布日期**: 2026-10-22
- **原文連結**: https://huggingface.co/blog/ibm-research/granite-timeseries-ensemble-r1

## 核心主題
IBM Research 推出 Granite Timeseries Ensemble，整合四種不同的預訓練時間序列模型架構，提供無需重新訓練的集合預測解決方案，減少選擇單一模型的猜測工作。

## 關鍵重點
- **四種模型成員**：整合 PatchTST-FM-r1（Patched Transformer）、PatchTST-FM-r2（Patched Conformer）、FlowState-r1.1（State-space model）和 TTM-r3（Tiny Time Mixers），各自捕捉趨勢、季節性和局部變化的不同方式。
- **兩種集合方法**：推薦的 Probabilistic Ensemble（等權重概率池化）和 IQR Ensemble（基於預測分散度的適應性權重），均無需訓練或調整權重超參數。
- **性能優勢**：在 GIFT-Eval 數據集評估中，集合方法在 MASE 指標上表現優於所有四個單一成員模型，提供更強的魯棒性。
- **易於使用**：透過 Hugging Face 可直接安裝 granite-tsfm 並載入預設集合配方，無需手動配置模型權重。

## 結論
Granite Timeseries Ensemble 為時間序列預測提供了一個簡單、魯棒且無需訓練的預設解決方案，特別適合希望避免選擇錯誤單一模型風險的開發者。雖然性能提升幅度不大，但其主要價值在於提供一致且可靠的預測結果。
---

檔案已成功儲存至指定路徑。
