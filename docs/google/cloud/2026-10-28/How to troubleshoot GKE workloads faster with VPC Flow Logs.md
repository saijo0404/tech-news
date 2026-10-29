# How to troubleshoot GKE workloads faster with VPC Flow Logs

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-29
- **原文連結**: https://cloud.google.com/blog/products/containers-kubernetes/using-vpc-flow-logs-to-troubleshoot-gke-workloads/

## 核心主題
這篇文章介紹如何使用 Google Cloud 的 VPC Flow Logs 來更快地排查 GKE (Google Kubernetes Engine) 工作負載的問題，通過將臨時 IP 地址轉換為工作負載名稱，並提供工作負載級別的歸屬信息。

## 關鍵重點
- VPC Flow Logs 通過 GKE 元數據豐富流量記錄，即使 Pod 消失後也能保留工作負載、命名空間和服務信息，無需額外代理或側車
- 使用 Flow Analyzer 工具可以視覺化分析流量，通過工作負載名稱而非 IP 地址來映射微服務依賴關係，快速識別異常通信
- 提供三個實用案例：將 IP 地址轉換為工作負載名稱、鑽探單一服務以查看呼叫者分佈、找出跨區域通信的 Pod 以優化成本

## 結論
通過升級日誌桶到可觀察性分析並啟用 Flow Analyzer，可以輕鬆實現這些功能，無需額外部署。建議在測試環境先啟用內節點可見性，並根據需求配置採樣率和過濾條件以平衡可見性與成本。
---
