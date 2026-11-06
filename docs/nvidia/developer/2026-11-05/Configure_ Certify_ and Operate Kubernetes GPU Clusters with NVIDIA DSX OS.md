# Configure Certify and Operate Kubernetes GPU Clusters with NVIDIA DSX OS

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-11-05
- **原文連結**: https://developer.nvidia.com/blog/configure-certify-and-operate-kubernetes-gpu-clusters-with-nvidia-dsx-os/

## 核心主題
這篇文章介紹 NVIDIA DSX OS 如何幫助操作人員自動化 Kubernetes GPU 集群的配置、驗證與維護。

## 關鍵重點
- **三大核心工具**：AICR（AI Cluster Runtime）提供版本鎖定配置食譜，NVCRE（Cluster Readiness Engine）執行集群準備驗證，NVSentinel 持續監控 GPU、節點和網路健康狀況
- **自動化優勢**：支持配置漂移檢測、性能閾值認證（如帶寬≥300 GBps）和故障隔離，減少手動交接
- **明確責任分界**：NVCRE 負責歸因，NVSentinel 負責隔離修復，所有工具均為 Apache 2.0 授權並支持外部貢獻
- **操作人員仍需管理**：基準線變更批准、測試閾值設定以及自動化無法解決的故障處理

## 結論
NVIDIA DSX OS 為 Kubernetes GPU 集群管理提供完整的自動化解決方案，從配置到驗證再到維護，顯著提升集群可靠性與操作效率。
---