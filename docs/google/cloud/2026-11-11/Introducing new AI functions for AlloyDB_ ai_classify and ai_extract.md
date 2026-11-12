# Introducing new AI functions for AlloyDB: ai.classify and ai.extract

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-12
- **原文連結**: https://cloud.google.com/blog/products/databases/ai-classify-and-ai-extract-functions-in-alloydb-ai/

## 核心主題
Google 推出了兩個新的 AlloyDB AI 函數（ai.classify 和 ai.extract），允許直接在 SQL 查詢中進行文本分類和結構化數據提取，無需將數據導出到外部服務。

## 關鍵重點
- **ai.classify 函數**：可在 SQL 中直接對文本進行分類，支援單標籤和多標籤分類，可指定類別描述和少樣本提示，無需手動撰寫提示工程
- **ai.extract 函數**：將非結構化文本轉換為符合目標模式的結構化 JSON 數據，自動處理系統指令，支援 JSON Schema 或文字欄位列表
- **智能批處理**：透過智能批處理優化 AI 函數執行速度，自動將輸入分組為優化微批次，減少模型 token 消耗並提升查詢性能
- **多產業應用場景**：支援醫療（臨床記錄結構化）、金融（發票資訊提取）、法律科技（合約條款提取）、房地產（房產描述解析）等領域

## 結論
這些新功能讓 AI 能力直接整合到資料庫引擎中，無需將敏感數據跨越多個網路邊界，既提升了數據安全性和查詢性能，又降低了模型 token 成本，為企業提供了更高效的在資料庫內執行 AI 任務的方式。
---
