# IBM releases SOTA Granite Time Series PatchTST-FM-r2 model with commercial-friendly license

- **來源**: Hugging Face
- **發布日期**: 2026-09-09
- **原文連結**: https://huggingface.co/blog/ibm-research/ibm-releases-sota-granite-time-series

## 核心主題
IBM 發布了 Granite Time Series PatchTST-FM-r2 模型，這是目前性能最佳的零樣本時間序列預訓練模型，採用商業友好的開源授權。

## 關鍵重點
- **卓越性能**：在 GIFT-Eval  benchmarks 上表現優異，是零樣本、可複製模型中性能最佳者，排名第 2（CRPS 和 MASE 指標），在商業友好授權模型中排名第一。
- **創新架構**：採用 Conformer 架構，結合自注意力與時間卷積，支持 8192 步上下文，比前代模型 PatchTST-FM-r1 增加 30 個區塊。
- **商業友好授權**：雙重授權（Apache 2.0 和 OpenMDW 1.0），用戶可選擇任一授權，提供廣泛的商業使用權利。
- **功能豐富**：支援 99 分位數預測、缺失值補補、概率預測，可應用於需求預測、價格預測、能源負載、流量、遥測數據等多種時間序列場景。

## 結論
這是一個可立即投入生產環境的高性能時間序列基礎模型，特別適合需要零樣本泛化能力的場景。模型代碼、權重和推理管道全部開放，研究者與開發者可快速上手並部署到實際應用中。
---