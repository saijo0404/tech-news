# AICR v1.0: Open, stable, and verifiable GPU cluster configuration

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-10-06
- **原文連結**: https://developer.nvidia.com/blog/aicr-v1-0-open-stable-and-verifiable-gpu-cluster-configuration/

## 核心主題
NVIDIA AI Cluster Runtime (AICR) v1.0 發布了穩定且可驗證的 GPU 集群配置方案，提供版本鎖定、驗證過的配方，並建立跨 CLI、REST API、Go SDK 等公共接面的穩定相容性合約。

## 關鍵重點
- **四個核心能力**：Snapshot（記錄集群狀態）、Recipe（描述所需配置）、Bundle（渲染部署套件）、Validation（驗證集群是否符合配方），這些能力獨立運作以確保清晰的分責。
- **驗證儀表板**：提供即時驗證儀表板，可透過服務、GPU 型號、作業系統、工作負載意圖和平台搜尋配方，並檢視驗證證據。
- **生態系統整合**：Pulumi Labs 和 Mirantis 的 k0rdent 整合展示了如何透過不同基礎設施即程式碼和多集群管理工具消費相同的 GPU 集群配置。
- **v1.0 相容性規則**：定義了公共 CLI、REST API、Go SDK、套件佈局和實體圖式的相容性規則，移除或不相容變更穩定公共接面需要新的主要版本發布。

## 結論
AICR v1.0 為 GPU 加速 Kubernetes 集群提供了可重複、可驗證的配置合約，解決了組件相容性問題，並鼓勵貢獻者為未涵蓋的硬體和集群組合提出配方。

---