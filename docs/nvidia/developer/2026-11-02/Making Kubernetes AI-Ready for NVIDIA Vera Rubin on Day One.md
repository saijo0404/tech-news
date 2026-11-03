# Making Kubernetes AI-Ready for NVIDIA Vera Rubin on Day One

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-11-02
- **原文連結**: https://developer.nvidia.com/blog/making-kubernetes-ai-ready-for-nvidia-vera-rubin-on-day-one/

## 核心主題
NVIDIA 透過 AICR (AI Cluster Runtime) 驗證 Kubernetes 對 Vera Rubin GPU 硬體即開即用，包含訓練與推理配方的完整驗證。

## 關鍵重點
- AICR 簡化 Kubernetes 對 Vera Rubin GPU 的準備工作，捕捉調優配置為可重用配方
- 訓練與推理配方均通過部署、合規性驗證，跨節點 NCCL 全減法測試達 744.71 GB/s 帶寬
- 主要配置變更：R615.23 開源核模塊驅動、Ubuntu 26.04 + 64k-page 核、ConnectX-9 SuperNIC + BlueField-4 DPU
- 發現 go-nvlib 未映射 Rubin 架構導致 DRA driver kubelet plugin 循環重啟，三天內修復
- 訓練與推理驗證證據已公開於 NVIDIA/aicr v1.0.0

## 結論
NVIDIA Vera Rubin 配方目前為 Preview 階段，不具生產級支援，但已驗證可重複性，平台團隊可透過 AICR 工具快速部署和驗證。
---
