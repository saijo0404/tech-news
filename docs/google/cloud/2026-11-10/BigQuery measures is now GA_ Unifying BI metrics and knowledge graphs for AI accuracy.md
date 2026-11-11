# BigQuery measures is now GA: Unifying BI metrics and knowledge graphs for AI accuracy

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-11
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/bigquery-measures-ga-unifying-bi-metrics-and-knowledge-graphs/

## 核心主題
BigQuery measures 正式成為一般可用功能，將 BI 指標與知識圖表整合在單一模型中，解決 AI 代理在理解「發生了什麼」和「為什麼」方面的斷層問題。

## 關鍵重點
- **單一模型整合**：BigQuery measures 直接在知識圖表實體上定義指標，消除 BI 平台與知識圖表之間的隔閡，讓 AI 代理能同時獲取數值與關聯上下文。
- **指標鎖定粒度 (Grain-locked measures)**：確保每個實體只被計算一次，避免重複計數導致的數據治理問題。
- **更豐富的建模能力**：支援複合表達式與派生指標，可在圖表模型中定義複雜計算，並透過 BQ.SHOW_GRAPH_EXPAND_SCHEMA 讓 AI 代理自動發現指標。
- **跨事實表查詢優化**：透過 start_node 參數解決「裂縫陷阱」問題，確保每個事實表在獨立樹狀結構中評估其原生粒度。
- **業務意義附著**：使用 OPTIONS Clause 將描述、同義詞與擴展元數據直接嵌入指標定義，提升可發現性與一致性。
- **生態整合**：與 Data Studio、Knowledge Catalog、Data Agent Kit 等工具整合，實現從指標定義到自然語言查詢的全流程自動化。

## 結論
BigQuery measures 的正式推出，讓企業能從既有基礎架構出發，建立單一來源真實，同時滿足 BI 報表與 AI 代理的需求，大幅降低數據治理成本與維護負擔。
---
