# 實驗 TPU、GKE Managed DRANET 與多叢集推論閘道

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-02
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/experimenting-with-tpus-gke-managed-dranet-and-multi-cluster-inference-gateway/

## 核心主題
Google Cloud 技術作者示範如何結合 GKE Managed DRANET、Multi-cluster Inference Gateway 與 TPU v6e，建立跨區域 AI 推論工作負載的自動故障轉移架構，確保單一區域當機時服務不中斷。

## 關鍵重點
- **六大建築元件：DRANET 網路資源分配、跨區域推論閘道、Cloud Storage FUSE、GKE Fleets 與 TPU v6e**：GKE Managed DRANET 讓 Pod 能直接申請與分享 TPU 與 GPU 的網路資源；Multi-cluster Inference Gateway 搭配 gke-l7-cross-regional-internal-managed-mc 型內部負載平衡器，在多個 GKE 叢集間自動路由流量至最近區域並支援故障轉移；Cloud Storage FUSE 讓模型權重直接掛載於 GCS bucket 無需複製；GKE Fleets 統一管理跨區域叢集，TPU v6e（ct6e-standard-4t，2x2 Slice）提供高階 AI 運算。
- **七步部署流程：從 VPC 設定到推論閘道配置**：建立標準 VPC 與 proxy-only subnet、預留靜態內部 IP、配置 GCS FUSE bucket 並綁定 Kubernetes Workload Identity；建立兩區域 GKE 叢集並啟用 Gateway API 與 Cloud Storage FUSE CSI driver；為 TPU node pools 啟用 DRANET（`--accelerator-network-profile=auto`）；透過 Fleet 註冊建立全球網狀管理、設定配置中心（primary region）；部署 vLLM 推論伺服器於兩區域 TPU 節點，使用 ResourceClaimTemplate 精確請求 4 顆 TPU 與網路設備；透過 Helm 將兩區域部署整合為單一 InferencePool，配置 InferenceObjective 依 KV cache 等硬體指標路由至最佳可用區域。
- **自動故障轉移驗證與可觀測性**：當模擬主要區域當機（部署離線）時，Gateway 自動偵測故障並無縫將所有使用者請求重新路由至次要區域叢集，確保流量不中斷；系統透過 AutoscalingMetric 追蹤硬體利用率（如 KV cache 使用量）作為健康檢查與負載平衡依據，而非僅依賴傳統 HTTP 健康檢查。

## 結論
此實驗展示 Google Cloud 如何以 K8s 生態系的創新功能（DRA、Inference Gateway、Fleets）結合自研 TPU v6e 與 GCS FUSE，打造「跨區域自動故障轉移」的 AI 推論基礎建設——模型權重不需複製、節點資源動態分配、流量路由依據硬體指標，為企業生產級 LLM 推論服務提供高可用、低延遲的參考架構，相關完整設定可於官方 Codelab 直接複製執行。
