# BigQuery Graphs with measures for trusted agentic workloads

- **來源**: Google Cloud Blog Data Analytics
- **發布日期**: 2026-08-14
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/bigquery-graphs-with-measures-for-trusted-agentic-workloads/

## 核心主題
當企業從簡單聊天助手轉向自主代理工作負載時，BigQuery Graphs 結合 measures 技術讓 AI 代理能在複雜業務關係中進行精確推理，解決扁平數據結構無法追蹤多跳業務情境的問題。

## 關鍵重點
- **關係的重要性**：傳統數據結構無法追蹤多跳業務情境，導致 AI 代理做出錯誤的運營決策，例如無法追溯銷售下降的原因
- **零 ETL 圖建模**：BigQuery Graph 允許將現有表直接映射為屬性圖，無需 ETL 即可統一治理指標與關係映射
- **原生 measures 支持**：數據模型師可在屬性圖 DDL 中直接定義 MEASURE（如 SUM 或 AVG），確保聚合計算準確性
- **視覺化圖模型器**：BigQuery Studio 內建無代碼拖放介面，讓開發者和業務用戶可直觀構建屬性圖
- **對話分析整合**：用戶可自然互動，代理將自然語言問題轉換為精確的 GoogleSQL 或 ISO GQL 查詢
- **Looker 原生整合**：業務指標在數據層統一管理，避免分散的邏輯堆疊，實現 Core KPI 完全一致且可信

## 結論
BigQuery Graphs 通過將治理指標與關係映射統一，使 AI 代理能夠在複雜業務依賴中進行精確推理，同時提供零代碼工具降低使用門檻，並通過 Looker 原生整合確保指標一致性與企業 DevOps 工作流。

---