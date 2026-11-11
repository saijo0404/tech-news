# Experimenting with ClusterNetworkPolicy in GKE

- **來源**: Google Cloud Blog Developers & Practitioners
- **發布日期**: 2026-11-11
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/experimenting-with-clusternetworkpolicy-in-gke/

## 核心主題
這篇文章介紹了如何在 Google Kubernetes Engine (GKE) 中使用 ClusterNetworkPolicy (CNP) 來實現更細粒度的網路政策控制，並通過三層架構（管理層、網路政策層、基準層）來平衡安全與自主性。

## 關鍵重點
- **三層政策架構**：CNP 採用管理層（最高優先級，強制安全規則）、網路政策層（中間優先級，開發者管理的命名空間政策）、基準層（最低優先級，預設拒絕策略）的三層架構，實現更精細的網路控制。
- **實例實驗**：作者通過實例實驗展示了如何限制對 LLM 命名空間的流量，僅允許授權客戶，並阻止對元數據 API 的集群級訪問（DNS 端口 53 除外），使用 TPU v5e 和 Gemma 4 模型。
- **可視化驗證**：利用 Hubble eBPF 流和 GKE 網路記錄實現即時政策驗證，可監控允許/拒絕的決策並維持合規性。

## 結論
ClusterNetworkPolicy 為 GKE 提供了更強大的網路安全控制能力，但實施時需要仔細規劃和設計規則以符合具體環境需求，特別是在平衡安全與自主性方面。
---
