# Building Federated Multimodal AI Workflows with NVIDIA FLARE

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-08-19
- **原文連結**: https://developer.nvidia.com/blog/building-federated-multimodal-ai-workflows-with-nvidia-flare/

## 核心主題
NVIDIA FLARE 透過支援參數高效（adapter-based）和完整模型通訊模式，協調跨多個資料中心的聯邦多模態 AI 訓練，解決資料分散與模型更新過大的挑戰。

## 關鍵重點
- **FedUMM 架構**：William & Mary 與 NVIDIA 合作開發的 FedUMM 系統，透過交換輕量 LoRA adapter 而非完整模型，將每輪通訊量從 28.6 GB 降至 0.094 GB，同時維持 97% 的模型表現。
- **大型物件外部化**：NVIDIA FLARE 支援將大型物件替換為輕量參考，並單獨傳輸底層資料，解決訊息大小限制問題。
- **Tensor 串流與磁碟後端聚合**：透過增量串流降低傳輸時記憶體壓力，並使用磁碟儲存聚合時的更新資料，避免伺服器記憶體隨客戶端數量線性增長。
- **更新合約設計**：必須明確定義哪些模型組件留在客戶端、哪些可傳輸、如何組合不同客戶端的更新，以及哪些指標回傳至伺服器。

## 結論
設計聯邦多模態 AI 工作流時，應優先定義更新合約並選擇合適的載入最小化策略。NVIDIA FLARE 提供的 Recipe API、Tensor Downloader 和磁碟卸載模組，為可擴展部署提供了經過驗證的解決方案。

---