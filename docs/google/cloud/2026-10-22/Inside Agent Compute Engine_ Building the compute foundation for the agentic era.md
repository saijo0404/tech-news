# Inside Agent Compute Engine: Building the compute foundation for the agentic era

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-23
- **原文連結**: https://cloud.google.com/blog/topics/ai-infrastructure/agent-compute-engine-deep-dive/

## 核心主題
Google 推出 Agent Compute Engine，以應對代理 AI 時代的基礎架構挑戰，提供每個 AI 代理硬件隔離的微 VM，兼具容器速度與 VM 安全性。

## 關鍵重點
- **硬件隔離微 VM**：每個代理擁有獨立硬件隔離環境，兼具容器速度與 VM 安全性，解決傳統計算架構無法支援數百萬規模代理工作負載的問題
- **零凭证架構**：沙箱內不儲存任何憑證、API 金鑰或 OAuth 憑證，確保企業數據安全與可審計性
- **四大工作負載類型**：支援互動式消費與企業代理介面、自主軟體工程工作區、大規模評估與強化學習、輕量型沙箱後端
- **效率優化**：應用感知閒置檢測（agent 閒置時幾乎零成本）、記憶體去重（DAX 與 CoW 技術共享 base image）、統一硬體池跨產品動態調度
- **持久化工作空間**：分層存儲（暫存數據、只讀共享卷、持久用戶工作區），支援 Google Workspace 與 VPC 整合，無需複製敏感數據
- **安全架構**：使用 Google Titan 和 Titanium IPU 提供硬件信任、代理身份治理（四種身份：使用者、授權、工作負載、工作人力）、端到端加密傳輸與靜止
- **大規模擴展**：支援 Gemini、Gemini for Business 及內部 RL 評估，時間彈性工作填補閒置時間，降低峰值硬體需求

## 結論
Agent Compute Engine 平台預計即將在 Google Cloud 上線，提供開發者對環境、身份、網路存取及生命週期的控制，為代理 AI 時代奠定堅實的計算基礎，使數百萬 AI 代理能夠在全球規模下快速啟動與高效運作。
---