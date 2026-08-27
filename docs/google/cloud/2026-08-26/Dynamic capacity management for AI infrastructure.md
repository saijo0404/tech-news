# Dynamic capacity management for AI infrastructure

- **來源**: Google Cloud Blog
- **發布日期**: 2026-08-27
- **原文連結**: https://cloud.google.com/blog/topics/ai-infrastructure/best-practices-for-dynamic-capacity-management/

## 核心主題
這篇文章介紹了動態容量管理的最佳實踐，幫助企業在單一靈活基礎設施上運行企業和 AI 應用，實現可預測的成本和性能。

## 關鍵重點
- **為計劃事件提前規劃容量**：使用 Dynamic Workload Scheduler 的 Calendar mode（時間表模式）或 Flex-start mode（彈性啟動模式），為重要事件或批處理工作預先確保 GPU、TPU 等關鍵資源。
- **建立故障轉移計劃**：為每個應用定義自動化的優先級硬件故障轉移列表，使用 Managed Instance Groups (MIGs) 和 Custom ComputeClasses，當首選配置不可用時自動切換到次選方案。
- **自動化整個容量管理生命周期**：透過 Google Kubernetes Engine (GKE) 的單一控制平面，實現從故障轉移列表到動態資源分配的完整自動化流程，包括動態資源分配以最大化硬件利用率。

## 結論
面對 AI 代理時代的挑戰，企業需要結合可預測的資源預先規劃與自動化響應機制，透過動態容量管理克服基礎設施限制，在控制成本的同時提升靈活性與效率。

---