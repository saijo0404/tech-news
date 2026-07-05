# Verifiable, private AI: Google Cloud expands Confidential Computing frontiers

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-23
- **原文連結**: https://cloud.google.com/blog/products/identity-security/verifiable-trust-in-the-ai-era-whats-new-in-confidential-computing/

## 核心主題
Google Cloud 宣布多項 confidential computing 創新——從全球規模的 Confidential G4 VM 到 Open-source Prompt Encryption SDK、Apple Private Cloud Compute 合作、Intel TDX 擴展至 C4 機型，以及 Confidential Space 獨立驗證與 H100 GPU 支援，全面強化 AI 時代的資料隱私與可驗證信任。

## 關鍵重點
- **Confidential G4 全球規模部署與 Prompt 加密 SDK**：Google Cloud 在 G4 機器系列（搭載 NVIDIA RTX PRO 6000 Blackwell 伺服器 GPU 與第 5 代 AMD EPYC Turin CPU）上提供 Confidential VM 與 Confidential GKE 節點，覆蓋所有標準 G4 可用區域，支援 On Demand、Reservations、DWS Flex Start 與 Spot/Preemptible 多種消耗模型。CPU-GPU 間資料傳輸全程加密，可解鎖 AI 推論、微調、HPC 與高限制資料場景，效能影響極小。同時，Google 將 Prompt Encryption SDK 開源至 GitHub，建立端到端加密通道——客戶端發送加密提示至 TEE 內推論伺服器，伺服器解密處理後加密回傳結果，確保提示與回應全程受密碼學保護。
- **Apple Private Cloud Compute 與 Intel TDX 擴展**：Google Cloud 與 Apple 合作擴展 Private Cloud Compute（PCC），整合 Google Confidential Computing、Intel TDX、NVIDIA Blackwell GPU、Titan 安全架構與共同開發的開源主機堆疊，滿足嚴格資料保護要求。同時，Intel TDX 即將以測試版形式導入 C4 機器系列（第 6 代 Intel Xeon 處理器），建立硬體隔離 Trust Domain 並支援遠端驗證。C3D 機型的 Confidential VM Live Migration 也正式通用。
- **Confidential Space 獨立驗證與 H100 GPU 支援**：Confidential Space 設計將工作負載操作者排除在信任邊界外。新增 Intel Trust Authority（ITA）作為獨立驗證服務（已通用），可在加密金鑰釋放前獨立驗證環境完整性。Confidential Space 現已支援 NVIDIA Hopper H100 GPU，使多方能共同Pooling 資料進行訓練與推論，同時保護個別資料不被其他參與者或 Google Cloud 存取，開啟隱私保護 Federated Learning 與聯合模型建構等應用。

## 結論
Confidential Computing 正在成為 AI 時代雲端計算的必要基礎設施——Google Cloud 以多層次策略（硬體隔離 TEE、密碼學端到端加密、獨立第三方驗證）將可驗證信任嵌入從晶片到平台的每一層。從全球規模的 Confidential G4、開源 Prompt SDK、Apple PCC 合作到 Confidential Space 的 H100 GPU 與 ITA 獨立驗證，Google Cloud 讓企業能在不犧牲效能與操作彈性下，安全地處理最敏感的 AI 與資料工作負載，推動隱私保護 AI 從理想邁向規模化部署。

---
