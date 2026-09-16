# Scaling Federated Learning Across Docker, Kubernetes, and Slurm with NVIDIA FLARE

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-09-15
- **原文連結**: https://developer.nvidia.com/blog/scaling-federated-learning-across-docker-kubernetes-and-slurm-with-nvidia-flare/

## 核心主題
NVIDIA FLARE 透過兩層架構實現跨 Docker、Kubernetes 和 Slurm 的聯邦學習，讓每個節點使用適合其基礎設施的執行後端。

## 關鍵重點
- **兩層架構設計**：NVIDIA FLARE 將持久化聯邦服務與動態啟動的任務工作員分離，使每個節點能使用 Docker、Kubernetes 或 Slurm 等適合其環境的執行後端，同時保留本地對資源分配、數據集、秘鑰和排程策略的控制權。
- **可移植資源規範**：任務透過可移植資源規範（portable resource specification）請求 GPU、CPU 單元和記憶體，與平台細節解耦，實現資源感知的執行。
- **研究隔離機制**：Studies 提供邏輯多租戶邊界，讓每個研究映射到本地的數據集、秘鑰、批准映像和排程策略，確保多個團隊在同一部署中不會混雜。
- **版本更新**：FLARE 2.8 引入 Docker 和 Kubernetes 部署支援，FLARE 2.9 新增 Slurm 支援，適用於 HPC 和共享 GPU 集群。

## 結論
NVIDIA FLARE 使異質基礎設施成為聯邦學習擴展的一部分，而非障礙，讓組織能在保留各自控制權的同時實現跨平台的協作。

---