# Serverless Managed Service for Apache Spark 3.0 新功能總覽

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-03
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/serverless-managed-service-for-apache-spark-runtime-3-0-features/

## 核心主題
Google Cloud Serverless Managed Service for Apache Spark 3.0 -runtime 以「速度、簡易、可靠」為核心，推出零設定上線、啟動時間縮短 75%、GPU 取得率改善、Spark 4.x 支援與跨區域增強等五大功能，降低大規模資料處理的基礎建設管理門檻。

## 關鍵重點
- **零設定上線大幅縮短「從專案到首次工作」的時間**：過去使用者建立 Serverless Spark 專案後仍需手動配置 IAM 角色、VPC 網路與防火牆規則才能提交第一份工作；3.0 runtime 自動配置必要的 IAM 角色與權限、自動啟用子網域的 Private Google Access 與系統防火牆策略，並將多個分散的 API 啟用簡化為單一「Managed Service for Apache Spark API」啟用，顯著降低入門門檻。
- **啟動時間縮短 75% 與 GPU 取得率提升**：3.0 runtime 將標準層與高階層的啟動時間縮短 75%，且無需任何程式碼或設定變更即可自動享有，使 Serverless Spark 能服務更多 SLA 敏感的互動式資料科學與批次管線；同時支援 Dynamic Workload Scheduler（DWS）Flex Start 模式，當 NVIDIA A100、L4 等高需求加速器Unavailable 時，系統將請求排入佇列並等待 GPU 容量可用，大幅提升延遲敏感 AI/ML 工作負載的取得率與可靠性。
- **Spark 4.x 首選支援與跨區域高可用性**：3.0 runtime 原生支援 Apache Spark 4.x 創新功能（含 Spark Connect 的解耦用戶端-伺服器架構）；預設啟用跨區域支援，可自動在單一區域內的多個區域分配執行節點以防止區域停機或硬體缺貨，且區域間網路流量不額外收費，消除傳統跨區域部署的成本負擔。

## 結論
Serverless Managed Service for Apache Spark 3.0 將「無伺服器」的理念推向更深層——從零設定上線到自動跨區域配置、從啟動效能大幅提升到 GPU 取得率優化，讓資料工程團隊能專注於資料處理與 AI 模型開發本身，而非基礎建設管理；資料科學使用量年增近一倍的成長趨勢，也印證了 Google Cloud 作為 Apache Spark 工作負載執行平台的競爭優勢。
