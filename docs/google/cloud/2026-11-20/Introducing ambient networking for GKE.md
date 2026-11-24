# Ambient networking for GKE: sidecarless service mesh

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-21
- **原文連結**: https://cloud.google.com/blog/products/networking/ambient-networking-for-gke-sidecarless-service-mesh/

## 核心主題
Google Cloud 正式推出 GKE ambient networking，以側邊車（sidecar）less 架構取代傳統服務網架，降低資源消耗與管理複雜度。

## 關鍵重點
- **架構轉變**: 將網路功能從每個應用 Pod 的側邊車移至共享節點組件，由 Traffic Director、Certificate Authority Service 等集中式控制平面管理。
- **零信任安全**: 自動建立 mTLS 加密與工作負載身份認證，強化服務間通訊安全性。
- **資源節省**: 移除側邊車後，L4 網架功能（如 mTLS、負載平衡）資源使用量最高可減少 10 倍。
- **簡化運營**: 無需 Pod 重啟即可升級代理版本，減少每年約 4 次的管理負荷與服務中斷。
- **豐富可觀測性**: 內建 L4/L7 指標，透過 Network Services Monitoring 自動收集流量模式、延遲與連線健康狀況。

## 結論
GKE ambient networking 代表服務網架的重要進化，透過完全管理的解決方案，讓開發者與平台運營人員能以更低成本、更高安全性部署服務間通訊，同時大幅降低資源消耗與運營複雜度。

---