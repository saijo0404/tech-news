# Support New AI Frameworks Faster Using NVIDIA Workload Map

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-11-02
- **原文連結**: https://developer.nvidia.com/blog/support-new-ai-frameworks-faster-using-nvidia-workload-map/

## 核心主題
NVIDIA Workload Map 提供統一的 Kubernetes 工作負載描述，使排程器、控制器和平台能夠跨框架解釋分佈式工作負載，無需維護框架特定的解析代碼。

## 關鍵重點
- Workload Map 提供預先構建的定義目錄，涵蓋 JobSet、PyTorchJob、RayCluster、RayJob、RayService、KServe、Knative、MPIJob、NVIDIA NIM、LeaderWorkerSet、Milvus、Grove PodCliqueSet 和 NVIDIA Dynamo 等多種 AI 框架
- 單一工作負載定義可支援工作負載檢查（Workload Map CLI）、群組排程（KAI Scheduler）和統一管理（NVIDIA Run:ai）
- 將工作負載知識從編譯器移至可開發、審查和應用的數據，減少框架特定解析器的需求
- Elotl 的 Nova 已採用 Workload Map 來解釋工作負載結構和資源需求，用於多集群排程決策

## 結論
NVIDIA Workload Map 是開源組件，可用於 NVIDIA DSX AI Factory GitHub 組織，支持多集群排程，幫助生態系統設計、構建和運營更高效的 AI 工廠。

---