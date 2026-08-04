# How to Run Isolated Tenant Kubernetes Clusters on Shared GPU Infrastructure

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-08-03
- **原文連結**: https://developer.nvidia.com/blog/how-to-run-isolated-tenant-kubernetes-clusters-on-shared-gpu-infrastructure/

## 核心主題
這篇文章介紹了如何使用 KAI Scheduler 和 vCluster 這兩款開源工具，在共享 GPU 基礎設施上運行多個完全隔離的 Kubernetes 租戶集群。

## 關鍵重點
- KAI Scheduler 提供基於頂層結構的 GPU 資源調度，支援每團隊配額和動態分配，可管理數千節點的 GPU 集群
- vCluster 為每個團隊提供虛擬化的 Kubernetes 集群，確保完整的邏輯隔離（獨立的 API 伺服器、CRDs 和 RBAC），同時共享底層節點和硬體
- 三個團隊（NLP、Vision、推薦系統）可各自擁有獨立的控制平面、RBAC、命名空間和 CRDs，並可擁有集群管理員權限，避免環境衝突
- 所有團隊共享同一個物理 GPU 節點（如 NVIDIA L40S），最大化基礎設施效率，無需物理分割硬體

## 結論
這種結合 KAI Scheduler 和 vCluster 的架構模式，在保持團隊自主性的同時避免了硬體分割，是實現多團隊 GPU 資源共享的理想解決方案，特別適合內部可信團隊的場景。

---