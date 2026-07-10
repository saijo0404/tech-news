# Autopilot Clusters with GKE managed DRANET_ GPUs and TPUs

- **來源**: cloud.google.com/blog
- **發布日期**: 2026-07-09
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/autopilot-clusters-with-gke-managed-dranet-gpus-and-tpus/

## 核心主題
Google Kubernetes Engine (GKE) 推出 Autopilot 集群與 managed DRANET 功能，支援 GPU 和 TPU 加速器的網路資源分配，包括 RDMA 網路介面，簡化 AI 工作負載的部署與管理。

## 關鍵重點
- GKE Autopilot 是 GKE 的 managed 版本，自動處理節點、縮放、安全性等預先設定，支援 GPU (B200) 和 TPU (v6e) 兩種加速器類型
- 透過 managed DRANET 可為 Pod 請求和分配網路資源，包括支援 TPU 和 Remote Direct Memory Access (RDMA) 的網路介面
- 設定流程包括建立 VPC、部署 Autopilot 集群、建立自訂 ComputeClass、ResourceClaimTemplate，並部署工作負載以引用這些資源
- 部署時會自動觸發 scale-up 操作，GKE Autopilot 會根據 ComputeClass 提供特定節點類型並配置 managed DRANET 網路，ResourceClaimTemplate 則作為橋接 Pod 與節點上加速器的連結

## 結論
透過 GKE Autopilot 與 managed DRANET 的整合，開發者可以更輕鬆地部署和管理基於 GPU 或 TPU 的 AI 工作負載，減少手動配置複雜度，並確保正確的網路資源分配。

---
