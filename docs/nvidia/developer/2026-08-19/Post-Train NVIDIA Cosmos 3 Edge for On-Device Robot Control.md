# Post-Train NVIDIA Cosmos 3 Edge for On-Device Robot Control

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-08-19
- **原文連結**: https://developer.nvidia.com/blog/post-train-nvidia-cosmos-3-edge-for-on-device-robot-control/

## 核心主題
這篇文章介紹了 NVIDIA Cosmos 3 Edge 模型，這是一個可部署在邊緣設備（如 Jetson Thor）上的 4B 參數世界模型，透過後訓練（post-training）技術將通用物理世界知識轉化為即時機器人控制策略。

## 關鍵重點
- Cosmos 3 Edge 是 4B omni-model（含 2B Nemotron 推理器），預訓練於相同物理世界數據，但模型體積適合在 Jetson AGX Thor 上運行
- 後訓練使用 nvidia/Cosmos3-DROID 數據集（76k 成功軌跡，約 350 小時數據），專注於機器人操作任務
- 在閉環模擬中達到 22.9% 的成功率，推理延遲約 1.53 秒/動作塊，支援即時邊緣部署
- 訓練需使用 NVIDIA DGX Station 配備 GB200/GB300 超級芯片，64 節點 x4 GB200 運行 60K 次迭代約需 68 小時
- 部署時使用 WebSocket 政策伺服器（OpenPI 協議），伺服器與客戶端均在機器人上運行，無需數據中心 GPU

## 結論
Cosmos 3 Edge 成功證明了 4B 世界基礎模型可以作為實用、實時、完全在機器人上運行的策略基礎，為邊緣機器人控制提供了新的可能性。
---
