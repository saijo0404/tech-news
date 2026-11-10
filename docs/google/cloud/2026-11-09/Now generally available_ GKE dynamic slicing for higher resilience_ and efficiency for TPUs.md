# Now generally available: GKE dynamic slicing for higher resilience, and efficiency for TPUs

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-10
- **原文連結**: https://cloud.google.com/blog/products/containers-kubernetes/gke-dynamic-slicing-on-tpus/

## 核心主題
Google 正式推出 GKE 動態切片功能，透過將邏輯 TPU 切片與物理節點池解耦，大幅提升 AI 工作負載的啟動速度和恢復速度，實現更高的 TPU 效能與韌性。

## 關鍵重點
- **啟動速度提升 5 倍**：透過即時組裝邏輯切片，大幅減少工作負載啟動時間。
- **恢復速度提升 4.5 倍**：故障隔離範圍縮小至 TPU 立方體，加速故障恢復。
- **兩種切片模式**：支援超切片（Super-slicing）與次切片（Sub-slicing），滿足不同規模工作負載需求。
- **資源利用率提升**：支援多租戶打包與部分健康節點池，最大化 TPU 資源利用。
- **零停機彈性**：無需刪除重建節點池，可動態組裝或分割 TPU 立方體。

## 結論
GKE 動態切片功能透過靈活的切片管理與故障隔離機制，為大型 AI 工作負載提供更高的韌性與運營效率，特別適合需要處理大規模訓練與推理工作負載的場景。此功能目前僅支援 TPU 全容量預訂模式，並在全球所有提供 TPU 的地區可用。
---
