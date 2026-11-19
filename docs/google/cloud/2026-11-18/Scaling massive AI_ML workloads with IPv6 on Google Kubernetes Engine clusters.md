# Run AI/ML workloads on IPv6-only GKE clusters

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-19
- **原文連結**: https://cloud.google.com/blog/products/networking/run-aiml-workloads-on-ipv6-only-gke-clusters/

## 核心主題
Google Cloud 推出單一堆疊 IPv6 支援，讓 GKE 集群和 Pod 都使用 IPv6，無需私有 IPv4 地址，解決 AI 部署面臨的 IP 地址短缺問題。

## 關鍵重點
- **無需私有 IPv4 地址**：節點和 Pod 使用 IPv6 獨家運行，避免與現存網路、VPC 或鄰近集群的 IPv4 地址衝突。
- **IPv4 互操作性**：透過 DNS64/NAT64 技術，Pod 可透明地訪問 IPv4 終端端、註冊表和數據集中心。
- **龐大地址空間**：每個節點提供 /112 網段（65,536 個地址），IP 地址容量不再限制集群、節點或 Pod 的擴展能力。
- **廣泛的加速器支援**：支援 Cloud TPU v6e (Trillium) 及多種 CPU 機型家族（E2、N1、N2、N2D、N4、C3、C3D、C4、C4D、C4A、Z3）。
- **直接工作負載可觀測性**：每個 Pod 擁有唯一 IPv6 地址，無需集群內 NAT，簡化遥測、網路策略和除錯。

## 結論
單一堆疊 IPv6 是大型 AI 部署的遊戲改變者，可立即在 GKE 1.37.1-gke.3020000 版本中開始使用。內部測試顯示，Pod 生命週期、網路延遲和服務負載平衡均與 IPv4 持平，無額外數據平面開銷。

---