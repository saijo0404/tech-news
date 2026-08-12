# ClusterNetworkPolicy in GKE: Balancing control and autonomy for your microservices

- **來源**: Google Cloud Blog
- **發布日期**: 2026-08-11
- **原文連結**: https://cloud.google.com/blog/products/networking/new-clusternetworkpolicy-in-gke/

## 核心主題
Google Cloud 推出了 ClusterNetworkPolicy (CNP)，這是 Kubernetes 的開源標準，用於在 GKE 中實現集中式的網絡安全策略管理，平衡開發者自主權與平台/安全團隊的合規需求。

## 關鍵重點
- **三層級架構設計**：引入 admin tier（最高優先級）、network policy tier（標準命名空間級別）和 baseline tier（最低優先級），解決政策衝突問題
- **明確的 Pass 動作**：允許安全團隊檢查流量並將最終 Accept/Deny 決策下放給開發者的命名空間政策，實現中央監督與分佈式管理
- **常見場景解決方案**：支持隔離敏感工作負載、保護核心服務、管理外部出站流量等場景
- **開源標準基礎**：基於 Kubernetes SIG-Policy WG 標準設計，確保安全性配置可移植性
- **預覽階段**：目前處於版本 1.36 及以後的預覽階段

## 結論
ClusterNetworkPolicy 將工作負載網絡安全從命名空間範圍規則提升到統一的集群級治理，同時保持開發團隊所需的運營靈活性，是平衡多租戶 Kubernetes 環境中開發者需求與安全合規需求的重要解決方案。
---
