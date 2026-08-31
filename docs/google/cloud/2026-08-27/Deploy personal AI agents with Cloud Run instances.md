# Deploy personal AI agents with Cloud Run instances

- **來源**: Google Cloud Blog
- **發布日期**: 2026-08-28
- **原文連結**: https://cloud.google.com/blog/products/serverless/introducing-cloud-run-instances/

## 核心主題
Google 推出 Cloud Run instances，讓開發者能以低成本、高性能的方式運行長久運行的 AI 代理等狀態性工作負載。

## 關鍵重點
- Cloud Run instances 提供單一實例運行環境，不自動縮放，適合需要持續運行的 AI 代理
- 支援最多 7 天連續運行，可手動停止並隨時重新啟動，成本為每月$5.70（1 vCPU + 1 GiB 記憶體）
- 每個實例都有固定的 HTTPS URL，跨更新和重新啟動不變
- 支援 OpenClaw 等個人 AI 代理的部署，可透過單一命令快速部署
- 使用共享 vCPU 和 vCPU 衝刺預算，適合非持續高運算負載的工作

## 結論
Cloud Run instances 為需要長期運行的 AI 代理提供了經濟高效且高性能的解決方案，特別適合個人開發者和小型團隊使用。
---