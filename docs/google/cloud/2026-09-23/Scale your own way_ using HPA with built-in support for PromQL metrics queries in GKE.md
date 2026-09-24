# Scale your own way, using HPA with built-in support for PromQL metrics queries in GKE

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-24
- **原文連結**: https://cloud.google.com/blog/products/containers-kubernetes/native-support-for-prometheus-metrics-in-gke/

## 核心主題
GKE 現在原生支援 Prometheus 指標，允許使用 PromQL 查詢自訂自動擴展觸發器，取代過去需要第三方適配器的複雜設定。

## 關鍵重點
- **無需第三方適配器**：GKE 可直接從 Cloud Monitoring 讀取 Prometheus 指標，無需部署 Stackdriver Custom Metrics Adapter 等外部適配器，降低管理複雜度。
- **支援複雜擴展場景**：可基於 Pub/Sub 未處理訊息數量、QPS、95 百分位回應時間等複雜指標進行自動擴展。
- **低延遲與低資源消耗**：控制器僅在需要時啟動，每 15 秒同步一次指標，確保快速擴展反應且無額外資源負擔。
- **支援 HPA scale-to-zero 功能**：可根據需求將工作負載擴展至零副本，並利用 CapacityBuffers API 快速恢復。

## 結論
此功能目前處於預覽階段，透過原生支援 Prometheus 指標，GKE 提供更強大、性能更好且操作更簡便的自動擴展體驗，幫助開發者更靈活地管理工作負載。

---