# Diagnose Distributed AI Workload Failures with NVIDIA Attribution

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-11-02
- **原文連結**: https://developer.nvidia.com/blog/diagnose-distributed-ai-workload-failures-with-nvidia-attribution/

## 核心主題
NVIDIA Attribution 是一個開源工具，用於將工作負載範圍內的日誌、指標和排程器狀態進行關聯，以在您的集群上產生可重現的診斷。

## 關鍵重點
- 系統包含兩個可部署組件：Attribution Service（提供 REST API 的核心歸因引擎）和 Attribution Blueprint（Python 參考調度器，連接集群調度器和遥測源到服務）
- 系統每周分析數百萬個工作負載，跨數十万個 GPU，已識別出特定主機和交換機端口周圍的組件故障模式
- 歸因過程遵循四個階段：確定工作負載範圍、收集觀察值、通過確定性規則提取和關聯事件、返回包含終端狀態和歸因領域的結構化結果

## 結論
NVIDIA Attribution 是工作負載中心的故障歸因系統，已在使用於 NVIDIA AI 基礎設施的生產環境中多年。它幫助團隊了解工作負載失敗的原因，並提供指導下一步行動的證據。
---