# Fine-tuning a 350M Model for Better Structured Outputs in 100 GRPO Steps

- **來源**: Hugging Face Blog
- **發布日期**: 2026-09-03
- **原文連結**: https://huggingface.co/blog/grpo-with-trl-ifstruct

## 核心主題
這篇文章介紹了如何使用 Group Relative Policy Optimization (GRPO) 方法，僅用 100 個訓練步驟和 500 個樣本，就能將一個 3.5 億參數的小模型在結構化輸出任務上的表現從 22.6% 提升至 29.7%。

## 關鍵重點
- 使用 LFM2.5-350M 模型配合 LoRA 技術，針對 IFStruct 基準測試進行任務特定微調，訓練參數僅佔原模型的 1.66%
- 定義三個獎勵函數（JSON 格式、欄位數量、Schema 驗證）來指導模型學習正確的結構化輸出格式
- 訓練後模型在 IFStruct 基準測試上的表現從 22.6% 提升至 29.7%，JSON 格式通過率從 18.0% 大幅提升至 31.9%

## 結論
即使是輕微的任務特定微調，也能顯著提升小模型在結構化輸出任務上的可靠性，縮小與更大模型之間的差距。此方法適合資源有限的開發者，可在免費 GPU 上實現。

---