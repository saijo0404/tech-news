# Accelerating agentic RL and evaluation research velocity with 45x faster GKE Agent Sandbox

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-30
- **原文連結**: https://cloud.google.com/blog/products/containers-kubernetes/accelerate-agentic-rl-with-gke-agent-sandbox/

## 核心主題
Google 推出專為強化學習（RL）優化的 GKE Agent Sandbox，解決 AI 實驗室在擴展代理強化學習時遇到的沙箱冷啟動慢、圖片拉取瓶頸和控制平面飽和等基礎設施瓶頸，實現 45 倍更快的沙箱啟動速度和 3 倍更少的控制平面切換。

## 關鍵重點
- **10x-45x 更快的首次命令時間（TTFC）**：GKE 可在 1-9 秒內啟動沙箱環境，相比原始 Kubernetes 的 44-85 秒平均時間，大幅減少 GPU 閒置時間。
- **尾延遲降低**：最壞情況下的沙箱等待時間從 7.5 分鐘減少到 10 秒以下。
- **3x 更少的控制平面切換**：SDK 的在位回收策略重新使用 Pod，減少 3.1 倍的 Pod 創建，保持 Kubernetes API 伺服器穩定。
- **支持高卡片數量的容器映像**：即使處理數千個大型映像（>1.2GB），也能有效支援 RL 和評估工作負載。
- **提供 Agent Sandbox RL 編排 SDK**：暴露乾淨的異步 Python API，並與 Gymnasium、NVIDIA NeMo Gym 和 OpenHands 等 RL 工具原生整合。

## 結論
GKE Agent Sandbox 已成為前沿 AI 實驗室（如 Mistral AI）的訓練基礎設施，使大規模代理 RL 軌跡和評估能夠可靠地同時運行，顯著加速研究速度。
---
