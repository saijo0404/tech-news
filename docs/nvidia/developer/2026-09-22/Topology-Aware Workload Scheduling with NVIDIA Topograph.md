# Topology-Aware Workload Scheduling with NVIDIA Topograph

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-09-22
- **原文連結**: https://developer.nvidia.com/blog/topology-aware-workload-scheduling-with-nvidia-topograph/

## 核心主題
NVIDIA Topograph 是開源工具套件，用於發現並歸一化集群拓撲，協助工作負載管理器進行拓撲感知排程。

## 關鍵重點
- 自動發現集群拓撲並發布為 Kubernetes 節點標籤、Slurm 配置或 Slinky ConfigMaps，支援雲端與本地環境
- 支援 Kubernetes Helm 部署、Slurm 配置生成及 KAI Scheduler 整合，可改善 GPU 工作負載放置
- 提供物理網絡當前地圖，透過 KAI Scheduler/Kueue 提升 AI 效率、能效比與成本效益

## 結論
NVIDIA Topograph 提供自動化的拓撲感知排程解決方案，可顯著提升 AI 工作負載的效率、能效比與成本效益，適用於雲端與本地集群環境。

---