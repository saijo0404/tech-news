# Validate GPU Cluster Readiness Before AI Workloads Land

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-09-23
- **原文連結**: https://developer.nvidia.com/blog/validate-gpu-cluster-readiness-before-ai-workloads-land/

## 核心主題
NVIDIA Cluster Readiness Engine (NVCRE) 是一個開源 Kubernetes 控制器，透過運行真實的分佈式工作負載來驗證 GPU 集群的生產準備狀態。

## 關鍵重點
- NVCRE 使用分層 API（Certification、Workflow、Job）將失敗歸因於特定節點和類別（如 NCCL 通信或 NeMo 預訓練）
- 自適應故障隔離自動分割失敗組並重新運行測試，識別可疑節點而非歸咎於整個組
- WorkloadRun API 處理 Kubernetes 上多節點 GPU 工作負載的設置，包括平台檢測、框架特定運行時配置和可選的群組調度

## 結論
NVCRE 與 NVIDIA AI Cluster Runtime 和 NVSentinel 整合，構成了 NVIDIA DSX OS 操作層，幫助團隊在生產工作負載落地前驗證 GPU 集群。

---