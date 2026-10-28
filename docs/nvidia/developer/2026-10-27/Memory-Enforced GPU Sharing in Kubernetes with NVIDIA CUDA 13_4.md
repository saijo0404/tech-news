# Memory-Enforced GPU Sharing in Kubernetes with NVIDIA CUDA 13.4

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-10-27
- **原文連結**: https://developer.nvidia.com/blog/memory-enforced-gpu-sharing-in-kubernetes-with-nvidia-cuda-13-4/

## 核心主題
這篇文章介紹了如何使用 NVIDIA CUDA 13.4 和 KAI Scheduler 實現基於工作負載的 GPU 記憶體強制共享，通過 GPU Fractioning Operator 實現記憶體限制和計算模式管理。

## 關鍵重點
- CUDA 13.4 引入了透明的記憶體邊界強制功能，提供精確記憶體量、保證最小值與可突衝最大值
- GPU Fractioning Operator 是新的開源 Kubernetes 操作員，可設置和監督多進程服務 (MPS)，並應用每工作負載的記憶體限制和計算模式
- KAI Scheduler v0.18.0 通過 NvFractions GPU 共享模式整合 GPU Fractioning，支持通過 Pod 註記指定記憶體請求、限制、計算模式和 GPU 設備分配
- 支持兩種記憶體請求方式：絕對大小和 GPU 部分比例，以及兩種計算共享模式：時間切片和 SM 共享
- 允許工作負載使用可選的突衝限制和計算模式選擇，並可跨多個 GPU 設備分配

## 結論
這項技術使平台團隊能夠以更少的基礎設施服務更多工作負載，通過精確的記憶體限制和靈活的計算共享模式，優化 GPU 資源利用率。
---
