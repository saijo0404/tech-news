# Build a Validated Kubernetes Runtime for NVIDIA Dynamo

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-10-30
- **原文連結**: https://developer.nvidia.com/blog/build-a-validated-kubernetes-runtime-for-nvidia-dynamo/

## 核心主題
這篇文章介紹了 NVIDIA AICR (AI Cluster Runtime) v1.0.0 如何將 Dynamo 及其基礎設施打包為驗證過的 Kubernetes 運行時配方，適用於 NVIDIA GB200/GB300 NVL72 系統。

## 關鍵重點
- AICR 提供可重複的部署與驗證方式，確保 GPU 驅動、資源分配、排程、網路及監控等基礎設施正確配置
- Dynamo 1.4.2 支援兩種 Kubernetes 路由路徑：Dynamo Frontend Router（適合模型特定端點）和 Gateway API Inference Extension (GAIE)（適合平台團隊管理共享入口）
- 部署流程包含五個步驟：快照集群、生成 Dynamo 推理配方、渲染部署束、使用 Helmfile 或 GitOps 部署運行時、驗證安裝的運行時
- 組件版本清單包含 NVIDIA GPU Operator v26.7.1、Dynamo Platform 1.4.2 等 15 個組件，適用於 NVIDIA GB200/GB300 NVL72 系統
- 驗證項目包含集群基線、平台健康、加速器存取、排程與擴展、可觀測性等檢查項目

## 結論
NVIDIA AICR 為開發者提供了標準化、可驗證的 Kubernetes 運行時解決方案，確保 Dynamo 在生產環境中的穩定性和可觀測性，特別適用於大型 GPU 集群部署場景。
---