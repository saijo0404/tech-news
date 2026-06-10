# 擴展 AI 代理：將 ADK 部署至 GKE Autopilot 逐步指南

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-04
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/scaling-ai-agents-a-step-by-step-guide-to-deploying-adk-on-gke-autopilot/

## 核心主題
Google Cloud 提供完整逐步指南，示範如何使用 Agent Development Kit（ADK）建構技術代理程式、建置 Docker 映像檔，並安全部署至 GKE Autopilot，同時以 Workload Identity 取代硬編碼金鑰實現企業級認證。

## 關鍵重點
- **七步部署流程：從 ADK 開發到容器化與 GKE 部署**：文章詳細說明从零開始的完整流程——使用 uv 與 ADK CLI 建立代理程式（選擇 Gemini 2.5 Flash/Pro 作為後端並指定 Vertex AI）、本地測試 ADK Web UI、撰寫多階段 Dockerfile 將代理程式封裝為輕量映像檔、推送至 Artifact Registry，接著以 `gcloud container clusters create-auto` 建立 GKE Autopilot 叢集並將 Deployment（預設兩份執行個體）、Service 套用至叢集，最終透過 `kubectl port-forward` 或 API 呼叫（curl POST `/run` 端點）驗證代理回應。
- **Workload Identity 企業級安全認證取代 API 金鑰**：為避免硬編碼憑證風險，文章示範建立 IAM Service Account、授予 `roles/aiplatform.user` 權限至 Vertex AI、允許 Kubernetes Service Account 模擬 IAM SA，並在 `deployment.yaml` 中以 `iam.gke.io/gcp-service-account` annotation 綁定，使 Pod 能以身分模擬方式安全存取 Vertex AI API。
- **Gateway API 與 HTTPS Load Balancer 生產級外曝**：選用步驟 7 示範如何以 GKE Gateway API（取代傳統 Ingress）搭配 Google 受管理 TLS 憑證與保留的靜態 IP，建立 HTTPS 負載平衡器；設定 HTTPRoute 將流量轉送至 ADK Service 並配置 HealthCheckPolicy，憑證頒發後代理即活躍於 `https://api.yourdomain.com`，完成從本地開發到生產環境的完整部署。

## 結論
此指南為開發者提供從 ADK 代理原型到 GKE Autopilot 生產部署的端到端路徑，以 Workload Identity 確保安全、以 Gateway API 實現現代化網路架構，讓 AI 代理能水平擴展以因應需求，同時維持企業級安全標準；文章亦提醒使用者在完成練習後刪除所有資源以避免持續計費。
