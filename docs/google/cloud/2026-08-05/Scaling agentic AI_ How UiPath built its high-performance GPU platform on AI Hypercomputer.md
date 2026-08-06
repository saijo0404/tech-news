# Scaling agentic AI: How UiPath built its high-performance GPU platform on AI Hypercomputer

- **來源**: Google Cloud Blog
- **發布日期**: 2026-08-06
- **原文連結**: https://cloud.google.com/blog/topics/customers/how-uipath-built-its-high-performance-gpu-platform/

## 核心主題
UiPath 透過 Google Cloud AI Hypercomputer 架構重新設計基礎設施，建立高效能 GPU 平台以支援企業級代理 AI 和智能文件處理。

## 關鍵重點
- **共享 GPU fleet 架構**：從分散式集群轉向共享 GPU fleet，透過 ML Services (MLS) 平台平衡訓練與推理工作負載，解決尖峰工作負載問題。
- **實例優化策略**：使用 A3 VM 實例 (NVIDIA H100 GPU) 進行訓練，搭配 G4 VM 實例 (NVIDIA RTX Pro 6000) 進行推理，優化成本效能比。
- **供應瓶頸解決方案**：利用 Google Cloud Dynamic Workload Scheduler (DWS) 提前預訂 GPU 容量，解決高階 GPU 供應不足問題。
- **客戶驗證成果**：Omega Healthcare 透過 UiPath 自動化超過 1 億筆交易，準確率達 99.5%；Thermo Fisher Scientific 自動化處理 53% 的發票，處理時間縮減 70%。

## 結論
UiPath 透過從被動配額轉向可預測的高效能引擎，成功將 GPU 資源視為共享戰略資源，大幅降低營運成本並提升 AI 工作負載的可靠性。工程師可透過 GitHub 工程模式複製此架構，並透過 Google Cloud G4 VM 實例進一步優化推理工作負載。

---