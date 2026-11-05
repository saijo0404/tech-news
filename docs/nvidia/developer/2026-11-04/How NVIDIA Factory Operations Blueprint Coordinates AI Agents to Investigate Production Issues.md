# How NVIDIA Factory Operations Blueprint Coordinates AI Agents to Investigate Production Issues

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-11-04
- **原文連結**: https://developer.nvidia.com/blog/how-nvidia-factory-operations-blueprint-coordinates-ai-agents-to-investigate-production-issues/

## 核心主題
NVIDIA 推出 Factory Operations Blueprint (FOX)，提供參考架構讓開發者建立工廠管理代理，透過協調多個專業代理來解決生產問題。

## 關鍵重點
- 工廠管理代理使用 NVIDIA Nemotron LLM、NemoClaw 代理框架和 NVIDIA OpenShell 來解釋任務、管理持久化記憶並強制執行訪問政策。
- 專業代理包括視覺檢查代理（使用 NVIDIA Cosmos）、fleet 管理代理（使用 NVIDIA Isaac Sim 和 ROS 2）以及根本原因分析代理（使用 Kumo Anomaly）來檢查缺陷、安排返工並調查原因。
- 在 SMT 組裝線參考範例中，系統追蹤 AOI 警報，經過二次檢查、機器人運送至返工，並進行根本原因分析，產生包含證據和建議糾正行動的 PDF 報告。
- FOX 支援完全在 NVIDIA DGX Station 上部署，保持生產記錄、圖片、提示和調查結果在工廠網路內。
- 透過 Siemens 案例，生產規劃可節省高達 20% 成本，虛擬生產準備可減少上市時間高達 40%。

## 結論
FOX 幫助開發者建立工廠管理代理，連接證據、調查問題並協調糾正行動，減少停機時間並提高品質。

---

*本文摘要基於 NVIDIA Developer Blog 於 2026 年 11 月 4 日發布的文章。*