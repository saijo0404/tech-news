# Build Your Own Transaction Foundation Model for Financial Intelligence

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-16
- **原文連結**: https://developer.nvidia.com/blog/build-your-own-transaction-foundation-model-for-financial-intelligence/

## 核心主題
NVIDIA 提供完整開發範例，展示如何使用 GPU 加速工具鏈（cuDF、cuML、NeMo AutoModel）建構專用於金融交易資料的 Transformer 基礎模型，在詐欺偵測任務上比傳統 XGBoost 基線提升超過 40% 的 AP 指標。

## 關鍵重點
- **交易序列的 Transformer 建模**：傳統表格資料依賴手動特徵工程，而交易基礎模型將客戶的連續交易歷史（如薪資入帳、購物消費、通勤扣款等）視為序列資料，利用 Transformer 的自注意力機制捕捉遠端事件之間的關聯，學習到單一交易列無法表達的行為模式。
- **GPU 加速的完整開發流程**：從使用 cuDF 進行 GPU 加速資料處理、自訂領域 Tokenizer（每筆交易約 12 個語義 Token，詞彙量僅 6,251 個，遠優於 BPE 的 39 個 Token 與 50,257 詞彙）、以 NeMo AutoModel 預訓練 ~2900 萬參數的 Llama 解碼器，到提取 512 維嵌入向量並與下游 XGBoost 分類器結合，整個管線全數在 GPU 上執行。
- **下游任務的顯著提升**：在 IBM TabFormer 詐欺資料集上，結合原始表格特徵與基礎模型嵌入向量的混合模型，在測試集上將 ROC-AUC 提升 0.41%、AP（精確率 - 召回率曲線下面積）提升 41.76%——這意味著在相同人力審查容量下可偵測到更多詐欺交易。嵌入向量本身因缺乏事件層級資訊而表現不如基線，但與原始特徵結合後發揮互補效果。

## 結論
NVIDIA 的交易基礎模型開發範例提供了一套可自訂的端到端框架——領域 Tokenizer、Transformer 解碼器與嵌入驅動分類頭均可獨立替換，讓開發者能將此模式延伸至流失預測、客戶分群、生命價值回歸、信用評分等下游任務，為金融機構從傳統規則驅動轉向數據驅動的 AI 決策提供了加速路徑。

---
