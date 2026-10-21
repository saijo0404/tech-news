# Announcing llm-d 1.0: Open distributed inference for agents on Google Cloud TPUs and GPUs

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-21
- **原文連結**: https://cloud.google.com/blog/topics/ai-infrastructure/llm-d-1-0-an-open-source-stack-for-distributed-inference/

## 核心主題
Google 推出了 llm-d 1.0，一個開源的、基於 Kubernetes 的分佈式 LLM 推理堆疊，專為代理（agents）設計，可在 Google Cloud 的 TPU 和 GPU 上運行。

## 關鍵重點
- **多租户服務質量控制**：透過 llm-d 流量控制實現優先級和公平性感知的路由，幫助延遲敏感型請求和突發代理工作負載共享集群，滿足 SLO 而不互相影響。
- **上下文感知的路由**：llm-d 路由器追蹤每個快取前綴所持有的副本，根據負載和預測延遲進行選擇，防止前綴驅逐風暴。
- **分散式推理架構**：單一終端管理多個加速器池，支援 vLLM、SGLang 和 Google Cloud TPU/GPU 混合部署，無需模型重寫即可利用 TPU。
- **安全升級機制**：支援零中斷更新和 DisaggregatedSet，可獨立管理 prefill/decode 池，升級時不影響現有會話。
- **異步推理支援**：引入 llm-d-async-processor，可將背景工作負載（如 RL 訓練）與即時推理並行處理，提高加速器利用率。
- **生產級驗證**：已在 Gemini 平台、17,000 節點多區域 GKE 部署和 A3 Mega 集群上驗證，TTFT 提升 35%-40%，吞吐量提升 2.4-2.9 倍。

## 結論
llm-d 1.0 為團隊提供了一個可組裝、可生產級別的分佈式 LLM 推理解決方案，特別適合處理多步驟代理和強化學習工作負載。其開源特性允許自定義部署，並已通過多項生產環境驗證，可顯著提升推理性能。
---
