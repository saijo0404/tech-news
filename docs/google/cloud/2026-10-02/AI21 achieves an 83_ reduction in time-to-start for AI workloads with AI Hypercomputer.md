# AI21 achieves an 83% reduction in time-to-start for AI workloads with AI Hypercomputer

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-03
- **原文連結**: https://cloud.google.com/blog/products/containers-kubernetes/ai21-trains-its-models-on-ai-hypercomputer/

## 核心主題
AI21 透過採用 Google Cloud AI Hypercomputer 與 Kueue 排程器，成功將高優先級 AI 工作任務的等待時間從 72 小時大幅縮減至 12 小時，並完全消除了手動排程干預。

## 關鍵重點
- **資源碎片化問題**：AI21 原先面臨 GPU 資源碎片化問題，即使總容量充足，分散的資源塊仍無法滿足大型訓練工作需求，導致高優先級任務阻塞長達 72 小時。
- **Kueue 排程器整合**：AI21 選擇 Kueue 作為 Kubernetes 排程器，因其與 GKE 原生整合良好，無需替換核心組件，並支援彈性容量自動分配。
- **手動排程自動化**：透過 Kueue 自動化排程，手動排程干預從每週 20 次降至零，團隊領導者不再需要調解資源爭議。
- **AI Hypercomputer 優勢**：AI Hypercomputer 提供高利用率集群（接近 100%），透過 GKE 提供 GPU 硬體直接存取，並支援 Spot VM 與 Dynamic Workload Scheduler。
- **合作回饋循環**：AI21 與 Google Cloud 技術帳戶經理合作，成為 Kueue 設計夥伴，共同開發如公平分配排程 (AFS) 等新功能。

## 結論
AI21 透過採用 Google Cloud AI Hypercomputer 與 Kueue 排程器，不僅大幅降低工作等待時間，更將團隊精力從資源爭議管理轉回實驗迭代，實現了效率與產出雙重提升。
---
