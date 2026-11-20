# Introducing in-place migration to GKE Dataplane V2

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-20
- **原文連結**: https://cloud.google.com/blog/products/networking/gke-dataplane-v2-in-place-migration/

## 核心主題
Google Cloud 推出 GKE Dataplane V2 的預覽版，並提供「原地遷移」功能，讓符合條件的 VPC 原生集群能直接從 Dataplane V1 升級至 V2，無需建立並行集群。

## 關鍵重點
- **GKE Dataplane V2 架構**：基於 eBPF 和開源 Cilium，支援最多 15,000 節點（無網路策略時達 65,000 節點），大幅提升性能與可擴展性。
- **原地遷移功能**：透過單一 Google Cloud CLI 命令即可啟動遷移，GKE 會自動處理三個階段（資格檢查、啟動遷移、自動化滾動），無需手動移動工作負載。
- **適用限制**：僅支援 VPC 原生集群且運行 GKE 1.35 或更高版本，不支援基於路由的集群或運行 Calico 的集群。
- **測試建議**：預覽期間建議先在非生產或測試集群上測試遷移，以確保穩定性。

## 結論
GKE Dataplane V2 的推出標誌著 GKE 網路架構的重大升級，而原地遷移功能的推出則大幅降低了企業上手的門檻，使現代化工作負載的遷移變得更加簡單和高效。
---
