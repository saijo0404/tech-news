# 宣布 GKE Standby Buffer：提升節點啟動速度，不爆預算

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-01
- **原文連結**: https://cloud.google.com/blog/products/containers-kubernetes/gke-standby-buffers-speed-up-autoscaling-for-less-spend/

## 核心主題
Google Cloud 推出 GKE Standby Buffer 功能，在現有 Active Buffer 基礎上引入低成本暫停式容量緩衝區——節點預先初始化和映像預載後進入暫停狀態（釋放運算與記憶體成本），需求來襲時恢復速度比全新開機快兩到三倍，以個位數百分比的成本開銷達成近乎零延遲的 Pod 排程。

## 關鍵重點
- **Standby Buffer 運作機制：預備、暫停、快速恢復三階段**：節點被預先配置並完整初始化（安裝 Kubernetes DaemonSet 等必要元件、預載容器映像），隨後進入暫停狀態，僅保留持久化磁碟與 IP 位址成本，釋放運算與記憶體費用；當流量暴增時，暫停節點以兩到三倍於全新配置的速度恢復運作，完美銜接 Active Buffer 處理初始尖峰與 Standby Buffer 重新填充之間的間隔；重新填充的節點會先以 Active 狀態運作一段可配置時間，再進入暫停，提供持續流量期間的額外 Active 容量。
- **效能與成本實測：P99 延遲從數分鐘降至個位數秒數，節省高達 90% 成本**：在相同流量負載測試中，無 Standby Buffer 的叢集 P50/P95/P99 延遲被困於 4 至 6 分鐘；啟用 Standby Buffer 後，P50 延遲降至個位數秒數，P95/P99 短暫攀升至約一分鐘後迅速恢復至個位數秒數；兩者可分配核心成本相近，效能遠勝；Agent Sandbox 排程延遲達成亞秒級，與完全超量配置相比節省高達 90% 成本，Unico 架構師表示「就緒時間從數分鐘降至 30 秒」。
- **宣告式 API 取代複雜 Workaround，Active 與 Standby 協同最佳化**：過去為避免冷啟動延遲，需依賴操作複雜的 Balloon Pod 或降低 HPA 閾值造成資源浪費；GKE CapacityBuffers API 以宣告式方式定義緩衝區，取代所有手動 workaround；Active Buffer 負責覆蓋初始不可預測尖峰，Standby Buffer 處理持續負載並防止慢速冷啟動；兩者搭配可達成一秒級 Pod 排程延遲；建議使用 GitHub 上的 Buffer Simulator 工具來最佳化緩衝區大小配置。

## 結論
GKE Standby Buffer 將叢集自動擴展從「被動的冷啟動」升級為「主動的保險政策」——企業不再需要為了峰值效能而長期超量配置，也不必忍受傳統 Kubernetes 自動擴展的數分鐘延遲。透過 Active + Standby 雙層緩衝的協同設計、宣告式 API 的簡化操作、以及僅個位數百分比的額外成本，GKE 讓效能與成本這兩難抉擇真正成為歷史，適用於代理工作負載、批次作業、CI/CD 管線、遊戲伺服器及各類尖峰型應用。
