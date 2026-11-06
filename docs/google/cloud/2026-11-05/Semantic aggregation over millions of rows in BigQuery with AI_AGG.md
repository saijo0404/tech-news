# Semantic aggregation over millions of rows in BigQuery with AI.AGG

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-06
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/semantic-data-aggregation-with-bigquery-and-ai-agg/

## 核心主題
BigQuery 推出 AI.AGG 功能，可原生在資料庫內對数百万行未結構化數據進行語義聚合，解決 LLM 上下文窗口限制問題。

## 關鍵重點
- **多級批處理架構**: AI.AGG 自動處理行級驗證、上下文安全的批處理、並行推理與遞歸綜合，抽象掉複雜的 chunking 與平行執行工程。
- **多模態支援**: 原生支援文本與多模態輸入，可透過 BigQuery Object Tables 直接聚合雲端儲存中的數千張圖片，無需資料移動或轉碼。
- **企業應用案例**: 
  - 診斷分析高量級系統日誌，找出微服務系統性故障的定性根本原因
  - 建立「代理數據雲」，自動分類無標籤的支援工單並輸出 JSON 陣列
- **提示工程即資料工程**: 需遵循嚴格程式化輸出規範，包括明確輸出合約、上下文分隔符、失敗狀態設計與少樣本錨定。
- **治理與防護**: 支援 VPC 服務控制防止資料洩漏，提供上下文快取降低 token 成本，並有 10,000 token 輸出上限等防護措施。

## 結論
AI.AGG 將 BigQuery 的關聯式引擎與 Vertex AI Gemini 的宏觀推理能力結合，使企業數據庫從被動歷史指標存儲庫，轉變為能進行深度全面智能的活躍語義運行時， democratize 了 petabyte 規模的語義分析存取。
---

檔案已成功儲存至指定路徑。
