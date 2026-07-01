---
# AlloyDB AI Functions - now with revolutionary performance boosts and cost savings

- **來源**: Google Cloud Blog
- **發布日期**: 2026-07-01
- **原文連結**: https://cloud.google.com/blog/products/databases/boost-performance-and-lower-costs-with-alloydb-ai-functions/

## 核心主題
Google Cloud 宣布 **AlloyDB AI Functions** 迎來重大效能與成本突破——透過 **Smart Batching** 與 **Proxy Model 最佳化模式**，將 LLM 調用速度提升最高 **23,000 倍**、成本降低 **6,000 倍**，同時推出 `ai.summarize`、`ai.agg_summarize`、`ai.analyze_sentiment` 等新函數，讓 Gemini 的世界知識直接嵌入資料庫查詢中。

## 關鍵重點
- **AI Functions 功能擴展：從生成到情感分析**：AlloyDB 的核心 AI 函數（`ai.generate`、`ai.rank`、`ai.if`、`ai.forecast`）已正式 GA。新推出三款函數——①**ai.analyze_sentiment**：自動將文本情感分類為正面、負面或中性。②**ai.summarize**：將冗長文本濃縮為核心要點並保留原意。③**ai.agg_summarize**：聚合多行數據生成單一群組摘要（如產品評論整合），支援 `GROUP BY` 語句。開發者可直接在 SQL 中呼叫這些函數，無需維護複雜的知識提取管線。
- **Smart Batching 智能分批處理**：針對過去「每行資料呼叫一次 LLM」造成的成本與延遲瓶頸，AlloyDB 自動將 AI 函數呼叫分批處理，將 LLM 的 boilerplate 提示詞僅發送一次而非逐行重複。AlloyDB 智慧決定最佳批次大小——太小無法獲得效能增益，太大則可能膨脹提示詞導致幻覺或超出 token 限制。內建重試機制，**ai.if 與 ai.rank** 函數已支援，測試顯示最高可提升 **2,400 倍**效能（每秒處理 10,000 行）。
- **Proxy Model 最佳化模式：革命性的 23,000 倍加速**：對於 `ai.if` 函數，AlloyDB 引入**最佳化模式**——預先訓練一個輕量代理模型（proxy model），使用您的嵌入資料並針對特定 LLM 輸出訓練，直接在資料庫內部處理決策，大幅減少外部 LLM 呼叫。內部測試顯示：每秒可處理 **100,000 行**（**23,000 倍提升**）、成本降低 **6,000 倍**（低至 **1/10 美分**）。工作流程：使用 `PREPARE` 語句訓練代理模型 → `EXECUTE` 執行查詢 → 若準確度低則自動 fallback 至 LLM。

## 結論
AlloyDB AI Functions 的突破證明了「將 LLM 直接嵌入資料庫」不再只是概念驗證——透過智能分批與代理模型，開發者可以以極低的成本與延遲執行大規模 AI 驅動查詢。從智能過濾（如根據深度規格搜尋防水相機）到評論摘要生成，AlloyDB 將 Gemini 的理解力轉化為原生的 SQL 操作，讓 AI 功能成為資料庫的內建能力而非外部依賴。

---
