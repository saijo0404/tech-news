# NVIDIA PAIR Virtual Inference Router Expands Available Compute on Your Local Network

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-09-03
- **原文連結**: https://developer.nvidia.com/blog/nvidia-pair-virtual-inference-router-expands-available-compute-on-your-local-network/

## 核心主題
NVIDIA PAIR 是一個虛擬推理路由器，可將本地 AI 任務分發到本地網路上的相容系統，以緩解多代理瓶頸，支援 Ollama 和 LM Studio，無需修改代理或 harness。

## 關鍵重點
- **支援硬體廣泛**：包括 NVIDIA GeForce RTX 20 系列 GPU 及更新、RTX PRO 工作站 GPU、DGX Spark 和 Apple M4+ 矽晶片
- **效能顯著提升**：在五子代理演示中，三設備 PAIR 集群完成工作只需 8 分 48 秒，而單一 RTX Spark 筆記型電腦需要 18 分鐘
- **無需修改現有工具**：支援 Ollama 和 LM Studio 介面，代理 harness 無需任何變更即可使用
- **彈性集群管理**：支援 mDNS 自動發現、MTLS 加密，並根據節點準備狀態、引擎狀態、模型存在和 GPU 利用率進行即時排程
- **開放原始碼專案**：可下載測試版供 Windows、macOS 或 Linux 系統使用，並可檢視程式碼和貢獻改進

## 結論
NVIDIA PAIR 為家庭 AI 集群帶來了類似資料中心的體驗，同時保持本地推理工作流程的熟悉度。它透過將獨立推理請求分發到本地網路上的可用系統，有效解決了多代理工作負載瓶頸問題，讓使用者能更靈活地利用現有硬體資源。

---