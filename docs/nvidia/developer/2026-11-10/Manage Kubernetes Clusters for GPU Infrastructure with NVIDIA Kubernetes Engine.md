# Manage Kubernetes Clusters for GPU Infrastructure with NVIDIA Kubernetes Engine

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-11-10
- **原文連結**: https://developer.nvidia.com/blog/manage-kubernetes-clusters-for-gpu-infrastructure-with-nvidia-kubernetes-engine/

## 核心主題
NVIDIA 推出 NVKE 和 NVKR 兩個開源專案，協助 AI 工廠在 GPU 基礎設施上構建和運營管理 Kubernetes 服務，讓客戶透過 Kubernetes API 消費 GPU 容量。

## 關鍵重點
- **NVKR 負責構建軟體**：生產可重現的節點映像、容器映像和海馬圖表，記錄所有輸入以便重構。
- **NVKE 負責管理集群**：使用 NVKR 產生的工件來提供和管理 Kubernetes 集群，透過管理平面和 REST API 運作。
- **客戶無需直接處理 OS 映像**：AI 工廠發布包含機器映像、集群釋放和節點池釋放的釋放集，客戶只需選擇經過驗證的 Kubernetes 版本。
- **目前處於公共預覽階段**：採用 Apache 2.0 許可證，API 和行為可能會變更，不建議用於生產工作負載。

## 結論
NVIDIA 透過 NVKE 和 NVKR 這兩個開源專案，幫助 AI 工廠設計、構建和運營 GPU 基礎設施，同時讓客戶能透過熟悉的 Kubernetes 生態系統使用 GPU 資源。兩個專案目前仍在公共預覽階段，適合評估和測試，但尚未推薦用於生產環境。

---