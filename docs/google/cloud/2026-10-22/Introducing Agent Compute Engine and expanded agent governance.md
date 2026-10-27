# Introducing Agent Compute Engine and expanded agent governance

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-22
- **原文連結**: https://cloud.google.com/blog/topics/ai-infrastructure/introducing-agent-compute-engine-and-expanded-agent-governance/

## 核心主題
Google Cloud 推出專為 AI 代理設計的 Agent Compute Engine 計算服務，並擴展 Gemini for business 的代理治理功能，以支持更大規模、更安全的自主代理運行。

## 關鍵重點
- **Agent Compute Engine**：提供硬體隔離的 microVM 環境，支持快速啟動、暫停和恢復，每個代理擁有獨立的安全沙箱，使用 Titanium 硬體安全架構提供防禦深度。
- **擴展的代理治理**：引入 Agent Gateway、Agent Registry、Agent Identity 和 Agent 可觀測性，支持跨雲、跨端點（包括 Cloud Run、GKE、本地設備）的統一治理。
- **Agent Substrate**：開源執行時序，可運行於任何 Kubernetes 集群，提供 10 倍更高的計算密度和次秒級啟動，支持 Claude Code、OpenClaw 等框架。
- **跨雲治理擴展**：治理能力擴展至多雲和混合環境，支持 granular 成本控制、智能模型路由和可擴展策略。

## 結論
Google Cloud 通過推出 Agent Compute Engine 和擴展代理治理功能，為企業提供了一套完整的基礎設施解決方案，使自主代理能夠安全、高效地在全球範圍內運行，同時保持對代理行為的全面可觀測和可控。

---