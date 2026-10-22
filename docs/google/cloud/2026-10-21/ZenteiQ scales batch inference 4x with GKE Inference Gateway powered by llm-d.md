# ZenteiQ scales batch inference 4x with GKE Inference Gateway powered by llm-d

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-22
- **原文連結**: https://cloud.google.com/blog/products/containers-kubernetes/zenteiq-scales-physical-ai-inference-4x-with-gke-and-llm-d/

## 核心主題
ZenteiQ 利用 Google Kubernetes Engine (GKE) 和 GKE Inference Gateway 搭配 llm-d 框架，成功將其批處理推理吞吐量提升 4 倍，大幅加速了科學基礎模型的訓練數據生成。

## 關鍵重點
- ZenteiQ 是一家專注於物理 AI 的初创公司，正在構建理解物理定律和數學方程的科學基礎模型，需要大量推理數據來訓練模型。
- 原本使用標準的輪詢負載平衡，導致服務節點負載不均和重複計算，嚴重影響數據生成速度，吞吐量波動可達一半。
- 部署 GKE Inference Gateway 和 llm-d 後，實現了基於實時隊列深度和 KV 緩存利用率的智能路由，解決了負載不均和重複計算問題。
- 實施後取得了顯著成果：吞吐量提升 4 倍，日產出從 14.7 億增加到近 60 億生成 token，緩存命中率提升 14%。

## 結論
GKE Inference Gateway 搭配 llm-d 為 ZenteiQ 提供了可擴展、可預測的推理架構，使其能夠更有效地訓練科學基礎模型，並為其他工作負載提供了可參考的解決方案。
---
