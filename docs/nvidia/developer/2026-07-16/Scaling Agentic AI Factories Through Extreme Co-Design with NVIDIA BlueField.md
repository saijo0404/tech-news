# Scaling Agentic AI Factories Through Extreme Co-Design with NVIDIA BlueField

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-07-16
- **原文連結**: https://developer.nvidia.com/blog/scaling-agentic-ai-factories-through-extreme-co-design-with-nvidia-bluefield/

## 核心主題
這篇文章介紹了 NVIDIA 如何利用 BlueField-4 DPU、Vera BlueField-4 STX 儲存處理器和 DOCA 軟體平台，透過極致協同設計來支援代理式 AI（Agentic AI）工廠的擴展，將基礎設施處理從主機 CPU 中分離出來，以提升 GPU 利用率、降低延遲並增強多租戶隔離。

## 關鍵重點
- BlueField-4 DPU 提供最高 800 Gb/s 的網路連接性（Ethernet 或 InfiniBand），整合 64 核心 NVIDIA Grace CPU 和高頻寬 LPDDR5X 記憶體，可將網路、儲存、安全、遥測和控制平面服務從主機 CPU 中分離
- DOCA 軟體平台提供可編程基礎設施服務，包括 DOCA Host-Based Networking（HBN）、BlueField ASTRA、DOCA Memos（管理 KV Cache 共享）和 DOCA 安全服務，支援零信任存取和多租戶生命週期管理
- 透過將基礎設施處理移至 BlueField 領域，Vera CPU 可專注於代理執行，同時實現更高的 GPU 利用率、更可預測的延遲、更強的租戶隔離、每 token 成本更低以及每瓦特 token 數量更多

## 結論
NVIDIA BlueField 平台透過極致協同設計，將基礎設施轉為推理管道的一部分，使 AI 工廠能夠高效處理代理式 AI 工作負載，同時提升效能、安全性和靈活性。

---