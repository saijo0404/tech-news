# New AI agent observability and governance across BigQuery and Looker

- **來源**: Google Cloud Blog Data Analytics
- **發布日期**: 2026-11-14
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/enterprise-ai-agent-observability-with-bigquery-and-looker/

## 核心主題
Google Data Cloud 擴展了 AI 代理可觀測性和評估功能，提供對 BigQuery 和 Looker 中第一方數據代理以及第三方代理的统一可視性，幫助企業在生產環境中追蹤 AI 代理的推理過程、數據接觸情況與運行成本。

## 關鍵重點
- **統一可觀測性框架**：將所有第一方和第三方代理的遥測數據（log、metrics、traces）收集到 BigQuery，支持開發者和管理員工具分析
- **隱私保護機制**：操作遥測數據與對話內容分開，排除用戶提示、模型回應等敏感內容，並支持行級/列級安全策略
- **成本控制與 FinOps**：提供 token 和延遲追蹤、查詢字節掃描上限、每日輸入輸出 token 配額，防止意外支出
- **評估基準測試**：使用 Prism 工具進行準確性測試，將基準分數存入 BigQuery，與生產日誌並行分析

## 結論
Google Data Cloud 透過擴展的 AI 代理可觀測性和評估能力，幫助企業在將 AI 代理從實驗原型推向生產時，能夠統一追蹤代理行為、保護敏感數據、控制成本並驗證準確性，為大規模部署提供完整的支持。
---