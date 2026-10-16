# Temporal Serverless Workers on Cloud Run: Scale workers ahead of demand

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-16
- **原文連結**: https://cloud.google.com/blog/products/serverless/temporal-serverless-workers-on-cloud-run-worker-pools/

## 核心主題
Temporal Cloud 現在支援將 Temporal 伺服器無伺服器工作員部署在 Cloud Run 工作員池上，可根據任務隊列自動縮放工作員數量，無工作時可縮放到零。

## 關鍵重點
- **自動縮放的代理工作員**：AI 代理可運行多步驟鏈式 LLM 推理與工具呼叫，工作員可瞬間啟動處理突發負載，隊列清空後自動縮零。
- **長運行情況的工作流程**：支援追蹤實體資源長期狀態的「實體模式」，個步驟運算時間不一，工作員池可彈性縮放。
- **突發批次工作**：只在執行時收費，閒置時成本為零，適合報表生成、媒體轉碼等批次任務。
- **伺服器端檢測與推送通知**：Temporal 伺服器監控任務隊列延遲，透過推送通知自動調整工作員池規模。
- **工作員版本化管理**：每個工作員版本獨立部署於獨立工作員池，支援 PINNED（固定版本）與 AUTO_UPGRADE（自動升級）兩種策略。

## 結論
Temporal Serverless Workers on Cloud Run 目前處於預覽階段，提供簡化的部署與縮放管理，無需管理集群或自動縮放器，並比傳統實例收費模式每 vCPU 小時與 GB 小時成本低近 40%，適合需要靈活計算資源的 Temporal 工作負載。
---
