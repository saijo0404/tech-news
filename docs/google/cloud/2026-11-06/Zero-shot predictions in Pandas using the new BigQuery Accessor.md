# Zero-shot predictions in Pandas using the new BigQuery Accessor

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-07
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/bigquery-ai-functions-in-pandas/

## 核心主題
這篇文章介紹了如何使用 BigQuery 的 .bigquery 存取器，在 Pandas DataFrame 中直接調用 BigQuery 的 AI 功能，實現零射預測（zero-shot predictions），無需離開熟悉的 Pandas 介面即可進行機器學習工作流。

## 關鍵重點
- 使用 .bigquery 存取器，可以直接在 Pandas DataFrame 上調用 BigQuery 的 AI 功能，如 ai.predict()、ai.embed()、ai.forecast() 等
- 這些功能包括：向量嵌入生成、時序預測、自然語言分類、回歸預測等
- 背後機制：將 Pandas 操作轉換為 Google Standard SQL，在 BigQuery 基礎設施上執行基礎模型，然後返回標準 Pandas DataFrame
- 使用簡單：只需導入 bigframes 庫並設定 GCP 專案 ID，即可直接調用 AI 功能
- 支援多種 AI 功能：包括 embed()、similarity()、forecast()、classify()、predict() 等

## 結論
BigQuery AI 功能在 Pandas 中使機器學習擴展變得輕鬆，讓開發者可以在熟悉的 Python 生態系統中解決複雜的 AI 挑戰。

---