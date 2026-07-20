# Scaling Agentic AI Factories Through Extreme Co-Design with NVIDIA BlueField

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-07-16
- **原文連結**: https://developer.nvidia.com/blog/scaling-agentic-ai-factories-through-extreme-co-design-with-nvidia-bluefield/

## 核心主題
這篇文章介紹了 NVIDIA BlueField-4 DPU、Vera BlueField-4 STX Storage Processor 和 DOCA 軟體平台如何通過極端協同設計，支持代理式 AI 工廠的擴展，通過將基礎設施處理從主機 CPU 中分離出來，提高 GPU 利用率、降低延遲並增強多租戶隔離。

## 關鍵重點
- 代理式 AI 將推理擴展到分佈式工作流，需要基礎設施快速移動、保護、檢索和重用作業數據，使基礎設施成為推理流程的一部分
- BlueField-4 DPU 提供 800 Gb/s 以太網或 InfiniBand 連接性，64 核 NVIDIA Grace CPU，PCIe Gen6 和高頻寬 LPDDR5X 記憶體，相比 BlueField-3 將網路帶寬翻倍，提供最多 6 倍更多的計算性能
- DOCA 軟體平台提供可編程基礎設施服務，包括 DOCA Host-Based Networking、BlueField ASTRA、DOCA Memos 和 DOCA 安全服務，使基礎設施處理可編程和可部署
- Vera BlueField-4 STX 儲存處理器結合 Vera CPU、ConnectX-9 網路和 DOCA Memos，實現 AI 原生儲存和 KV Cache 管理，優化長上下文和代理式推理工作負載
- 基礎設施處理包括網路、儲存、安全、遥測和上下文管理，這些服務在 AI 工廠數據路徑中加速處理，不消耗主機 CPU 資源

## 結論
NVIDIA BlueField 平台通過加速基礎設施處理，使 AI 工廠能夠更好地支持代理式 AI 工作負載，提高互操作性、隔離性、GPU 利用率、每 token 成本以及每瓦特 token 數量，為下一代 AI 工廠提供強大的基礎設施解決方案。

---