# The future of orchestration: Pine59’s journey to Airflow 3 on Google Cloud

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-18
- **原文連結**: https://cloud.google.com/blog/topics/supply-chain-logistics/the-future-of-orchestration-pine59s-journey-to-airflow-3-on-google-cloud/

## 核心主題
Pine59 公司為了應對數據量增長，將其數據管道從 Airflow 2 升級到 Airflow 3，以提升 MLOps 能力、開發者工作流和管道速度。

## 關鍵重點
- 通過壓力測試 Managed Airflow (Gen 3) 架構，Pine59 發現了顯著的處理速度、任務調度和穩定性改進
- 通過設置專門優化模型推理的 GKE 集群，Pine59 優化了 ML 推理工作流的調度
- 利用 Airflow 3 的插件作者系統，Pine59 開發了自訂插件（如 BigQuery Auto-linkify 和 DAG Run Configuration Search）來提高開發者效率
- Daily Foot Traffic 管道的處理時間從近 38 分鐘減少到不到 26 分鐘，提升了約 32%

## 結論
Pine59 的轉型證明了升級到新一代調度系統可以顯著改善 MLOps 能力，並為未來的數據和 AI 管道奠定更快、更可靠的基礎。
---