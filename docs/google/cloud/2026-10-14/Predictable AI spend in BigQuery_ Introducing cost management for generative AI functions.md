# Predictable AI spend in BigQuery: Introducing cost management for generative AI functions

- **來源**: Google Cloud Blog Data Analytics
- **發布日期**: 2026-10-15
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/using-bigquerys-generative-ai-cost-management-features/

## 核心主題
Google Cloud 正式推出 BigQuery 生成式 AI 函式的基於 token 的日額配額管理功能，讓團隊可以在預算內創新。

## 關鍵重點
- 提供四項日額配額（AI 輸入 token、AI 輸出 token，分別為專案層級與每使用者層級），透過 Google Cloud IAM 配額系統管理
- 支援的函式包括 AI.GENERATE、AI.CLASSIFY、AI.IF、AI.SCORE 等，但不包含嵌入函式（如 AI.GENERATE_EMBEDDING）
- 管理方式：可透過 Google Cloud 控制台即時調整配額，或透過 Cloud Quotas API、gcloud CLI 及 Terraform 自動化管理
- 最佳實踐：使用 AI.COUNT_TOKENS 函式評估輸入數據，並根據實際使用情況調整配額以控制開支

## 結論
透過設定基於 token 的配額，團隊可以在 BigQuery 中使用生成式 AI 時擁有更可預測的開支控制，同時避免預算超支。

---