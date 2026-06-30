---
# Conversational Analytics in BigQuery now GA

- **來源**: Google Cloud Blog
- **發布日期**: 2025-06-30
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/conversational-analytics-in-bigquery-now-ga/

## 核心主題
BigQuery 語音分析（Conversational Analytics）正式通用化（GA），讓企業以自然語言直接在 BigQuery 中查詢資料、執行多步驟分析，並透過 Gemini 模型產生可信的視覺化報告。

## 關鍵重點
- **自然語言分析，打破資料孤島**：無需設定即可在 BigQuery Studio 和 Data Canvas 中使用，支援專案、資料集、表格、圖表等深度代理設定；可跨雲端分析 Lakehouse 管理的 Apache Iceberg 表格，以及 Databricks、AWS Glue、SAP 和 Salesforce 等來源，打破資料孤島。
- **可稽核的信任機制**：每項分析都基於 Knowledge Catalog（詞彙表、資料檔掃描）、BigQuery Graph 和經過驗證的查詢；提供可視化的思考步驟、原始來源引用、主動消除歧義，以及長期記憶能力，確保分析結果可追溯。
- **企業級安全與治理**：繼承 BigQuery 的治理模型，支援 Access Transparency、CMEK、Private IP、VPC Service Controls 和資料駐留保證（EU/US 多區域）；提供成本控管、查詢大小上限和 BigQuery 標籤用量追蹤。
- **從回答問題到主動調查**：Deep-dive 模式可自動規劃分析步驟、執行多步驟調查並產出完整報告；Agentic workflows 支援排程自主代理，每日/每週自動監控資料、偵測異常並推播洞察至聊天工具。
- **結合 BigQuery AI 函數**：代理可直接呼叫 AI.KEY_DRIVERS（根因分析）、AI.FORECAST（趨勢預測）、AI.DETECT_ANOMALIES（異常偵測），以及查詢物件表格中的非結構化資料（PDF、圖片、影片等）。

## 結論
BigQuery 語音分析 GA 標誌著企業正式告別靜態儀表板時代。透過將 Gemini 的深度推理能力嵌入資料倉儲，BigQuery 提供了真正的「行動系統」——不僅回答問題，更主動調查、產生洞察，同時內建企業級安全治理，讓每位員工都能以自然語言與資料對話。

---
