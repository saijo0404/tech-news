# Agent Substrate brings high-density, scalable, trusted infrastructure to GKE

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-16
- **原文連結**: https://cloud.google.com/blog/products/containers-kubernetes/agent-substrate-available-on-gke/

## 核心主題
Google 宣布在 GKE 上推出 Agent Substrate，這是一個專為自主代理設計的開源安全執行時序，可提供比標準容器運行時高 10 倍的密度。

## 關鍵重點
- **高密度與低延遲**：支援每秒超過 500 次暫停/恢復激活，沙盒環境可在 500ms 內恢復
- **原生零信任安全**：提供硬體隔離的 Cloud Hypervisor 微 VM 或 gVisor 沙盒，並具備動態網路控制
- **主動式計算經濟**：閒置代理可立即暫停並釋放資源，實現零閒置模型，每主機可容納超過 1000 個休眠代理
- **Kubernetes 基礎架構**：結合 Kubernetes 的自修復節點與自動擴展能力，同時提供代理原生數據平面

## 結論
Agent Substrate 為 AI 團隊提供了在 GKE 上構建可擴展、安全且高性價比的代理平台的清晰路徑，並已獲得 Nous Research 等領先 AI 團隊的採用。
---