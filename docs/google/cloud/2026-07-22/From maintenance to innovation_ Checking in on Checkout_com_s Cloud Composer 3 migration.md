# How Checkout.com tallies data with Cloud Composer 3

- **來源**: Google Cloud Blog Data Analytics
- **發布日期**: 2026-07-23
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/how-checkout-com-tallies-data-with-cloud-composer-3/

## 核心主題
Checkout.com 將自管理 Apache Airflow 環境遷移至 Google Cloud 的 Managed Service for Apache Airflow (Gen 3)，以提升可靠性、降低成本並加速開發者工作流。

## 關鍵重點
- **可靠性提升**：Managed Airflow 提供 DAG 隔離，單一 DAG 失敗不會影響整個環境，並提供更好的可視性與排錯能力。
- **成本節省**：透過動態縮放功能，根據工作負載自動調整資源，每月節省約 30% 成本。
- **開發者工作流改善**：DAG 同步時間大幅減少，dbt 執行更簡單，並可透過 Gemini Cloud Assist 進行 AI 輔助排錯。

## 結論
這次遷移讓 Checkout.com 的數據工程師能更專注於提供價值，並建立了更穩定、可擴展且成本效益更高的數據基礎設施。

---