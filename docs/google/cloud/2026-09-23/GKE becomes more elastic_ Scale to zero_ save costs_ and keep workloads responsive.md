# GKE becomes more elastic: Scale to zero, save costs, and keep workloads responsive

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-24
- **原文連結**: https://cloud.google.com/blog/products/containers-kubernetes/gke-adds-native-scale-to-zero-capabilities/

## 核心主題
GKE 1.37 引入原生 scale-to-zero 功能，讓工作負載可以完全縮放至零並快速恢復，降低閒置資源成本同時保持響應速度。

## 關鍵重點
- GKE 1.37 原生支援 scale-to-zero，取代複雜的 KEDA 解決方案，無需額外組件與大量 YAML 配置
- 透過 HPA 與 AutoscalingMetric 整合，可基於外部指標（如 Pub/Sub 未處理訊息）自動縮放工作負載
- 容量緩衝區（Capacity Buffers）解決冷啟動問題，將啟動延遲從分鐘級降至秒級，同時維持零成本

## 結論
啟用 GKE 原生 scale-to-zero 功能可大幅降低閒置資源成本，同時透過容量緩衝區保持工作負載的響應速度，是實現真正彈性架構的關鍵步驟。

---