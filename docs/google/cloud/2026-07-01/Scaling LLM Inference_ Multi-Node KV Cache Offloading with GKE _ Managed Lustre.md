# Scaling LLM Inference: Multi-Node KV Cache Offloading with GKE & Managed Lustre

- **來源**: Google Cloud Blog
- **發布日期**: 2026-07-01
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/scaling-llm-inference-multi-node-kv-cache-offloading-with-gke-managed-lustre/

## 核心主題
Google Cloud 提出在 **GKE 上結合 Managed Lustre 並行檔案系統與 llm-d offloading stack**，實現多節點 KV Cache 外掛——將注意力狀態外掛至高頻寬外部檔案系統以突破本地儲存容量限制，在六節點 A3 Mega 叢集上以 95% 快取命中率為 Llama-3.3-70B 推論減少近 **60% GPU 時數**、節省超過 **50% TCO**，並提供從部署到維運的完整生產藍圖。

## 關鍵重點
- **為何選擇 Managed Lustre 而非本機池化**：傳統將節點本地儲存池化（pooled NVMe）需叢集自行管理複雜資料分佈與跨節點複製；Managed Lustre 提供專屬的高效能外部並行檔案系統作為叢集級分散式快取層，繞過主機容量限制且消除管理本機池化驅動器的網路開銷。架構四大元件包含：GKE GPU 節點（專屬加速器）、Managed Lustre（集中式外掛層）、PVC Evictor（分散式垃圾回收）與 llmd-fs-connector（KV cache 外掛橋接）。
- **支援模型與部署流程**：支援 **Qwen3.5-35B-A3B**（block size 528）與 **Gemma 4-31B-it**（block size 256）。部署流程：建立 GKE 叢集（啟用 Lustre CSI）→ 建立 GPU 節點叢（a3-megagpu-4g / a4-highgpu-4g）→ 透過 StorageClass + PVC 開通 Lustre 儲存（9,000Gi 至 8,401,600Gi）→ 部署 vLLM 引擎（MultiConnector + llmd-fs-connector 參數）→ 部署 PVC Evictor（建議每 72 TB 部署 1 複本，高規模需 c4-standard-16 專用節點）。混合式 CPU RAM 延伸可再提升 **40% TTFT** 並降低 **30% 端到端延遲**。
- **PVC Evictor 高效能維運設計**：Evictor 以 Helm 部署，預設 16 個平行爬蟲執行緒、每批 5,000 檔刪除、大容量記憶體佇列（1M-2M）緩衝待刪檔案、10 分鐘未存取即淘汰；每 Pod 分配 12-15 CPU 與 8-16Gi 記憶體避免限流/OOM。支援分片擴展，多複本模式按快取命名空間分區防止競態條件。清理流程包含 Helm 卸載 → 刪除部署 → 刪除 PVC → 刪除叢集（Lustre reclaimPolicy=Delete 自動清理底層儲存）。

## 結論
Google 的 Managed Lustre + GKE + vLLM 組合為企業級 LLM 推論提供了一套經過驗證的**多節點 KV Cache 外掛生產方案**——不僅以 95% 命中率帶來實質的 GPU 成本節省（60% GPU 時數、50% TCO），還透過 PVC Evictor 的分散式垃圾回收、混合 CPU RAM 延伸與完整的部署/清理流程，確保系統在處理長上下文視窗與代理式 AI 工作負載時兼具高效能與可擴展性。

---
