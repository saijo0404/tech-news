# How Checkout.com tallies data with Cloud Composer 3

- **來源**: Google Cloud Blog Data Analytics
- **發布日期**: 2026-07-23
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/how-checkout-com-tallies-data-with-cloud-composer-3/

## 核心主題
Checkout.com 將自管理 Apache Airflow 環境遷移至 Google Cloud 的 Managed Service for Apache Airflow (Gen 3)，以提升可靠性、降低成本並提高開發者效率。

## 關鍵重點
- **自動化維護**：從自管理環境遷移至管理服務，大幅減少伺服器管理、補丁和事故應答的維護負擔
- **動態擴展**：根據工作負載自動調整資源數量，每月成本降低約 30%
- **DAG 隔離**：每個 DAG 運行在獨立環境中，單一任務失敗不會影響整個環境
- **更快的部署**：DAG 同步時間從約 6 分鐘減少到近乎即時，團隊無需平台支援即可上線
- **dbt 現代化**：使用容器化 dbt 運行，消除依賴瓶頸，無需手動管理虛擬環境

## 結論
這次遷移使 Checkout.com 的數據工程師能專注於價值交付，並建立了更穩定、可擴展且成本效益更高的數據基礎設施。

---
