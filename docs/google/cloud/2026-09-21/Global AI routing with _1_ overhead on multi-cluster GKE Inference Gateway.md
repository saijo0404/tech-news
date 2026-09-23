# Global AI routing with <1% overhead on multi-cluster GKE Inference Gateway

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-22
- **原文連結**: https://cloud.google.com/blog/products/containers-kubernetes/gpu-and-tpu-utilization-with-multi-cluster-gke-inference-gateway/

## 核心主題
Google 透過多集群 GKE 推理閘道實現全球 AI 負載平衡，在跨區域擴展時實現近乎線性的吞吐量提升，同時僅增加不到 1% 的過載。

## 關鍵重點
- **多集群 GKE 推理閘道架構**：在邊緣層處理全球多區域流量分佈和高可用性，下方使用 LLM-d 路由器處理複雜的記憶體感知排程演算法，使分散的區域集群像單一加速器隊列運作。
- **記憶體感知路由**：基於 KV 快取 token 利用率進行負載平衡，當區域達到 40% 利用率閾值時自動將溢流流量路由到下一個健康區域，無需人工介入。
- **測試結果**：在跨三個區域（us-east5、us-west8、europe-west4）的 17,000 個計算節點部署中，吞吐量從單集群的 0.72 req/s 增加到三集群的 2.10 req/s，成功率維持在 99.9% 以上。
- **極低的過載**：透過推理閘道路由流量僅增加不到 1% 的過載，提供 99.5% 的直接本地集群調用吞吐量，實現全球負載平衡幾乎零成本。

## 結論
這種架構成功將全球分散的計算能力整合為單一高效引擎，最大化每美元的智能，使團隊能夠在容量碎片化環境中充分利用加速器資源，而非讓資本浪費。

---