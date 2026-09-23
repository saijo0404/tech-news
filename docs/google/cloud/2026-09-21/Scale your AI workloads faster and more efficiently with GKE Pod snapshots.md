# Scale your AI workloads faster and more efficiently with GKE Pod snapshots

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-22
- **原文連結**: https://cloud.google.com/blog/products/containers-kubernetes/gke-pod-snapshots/

## 核心主題
Google 推出 GKE Pod snapshots 新功能，解決 AI 工作負載冷啟動問題，大幅提升啟動速度並降低資源浪費。

## 關鍵重點
- GKE Pod snapshots 可將 AI 推理啟動時間減少高達 89%，70B 參數模型只需 37 秒，8B 參數模型只需 15 秒
- 解決冷啟動問題，避免過量 provision 基礎設施，改為按需自動擴展
- 優化代理工作流和沙盒，可快速啟動和暫停沙盒，減少閒置成本
- 支援任何工作負載，包括複雜 Java 應用、遊戲伺服器或舊式單體應用

## 結論
GKE Pod snapshots 提供靈活的配置選項，可透過 Pod snapshot CRDs 定義策略，適用於任何需要快速啟動的工作負載，幫助企業在提升性能的同時降低成本。
---