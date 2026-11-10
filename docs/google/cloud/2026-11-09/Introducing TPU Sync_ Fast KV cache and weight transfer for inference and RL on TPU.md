# Introducing TPU Sync: Fast KV cache and weight transfer for inference and RL on TPU

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-10
- **原文連結**: https://cloud.google.com/blog/topics/ai-infrastructure/introducing-tpu-sync-fast-kv-cache-and-weight-transfer-on-tpu/

## 核心主題
TPU Sync 是一個開源庫，旨在解決 TPU 集群中模型狀態（KV 快取和權重）的管理問題，通過異步 DMA 傳輸將數據直接移動於 TPU HBM、主機 DRAM、共享儲存和數據中心網路之間，大幅降低 KV 傳輸延遲和首次生成時間。

## 關鍵重點
- **架構優勢**：採用布局保留的直接 DMA 和原地緩衝重疊，無需 XLA 編譯，支援高頻寬 PCIe DMA 和 DCN 串流
- **推理優化**：將主機 DRAM、本地 SSD 和 Google Cloud Managed Lustre 轉化為多層 KV 快取，大幅降低 KV 傳輸延遲和 TTFT
- **強化學習支援**：提供低層級 DMA 和 DCN 原語，讓 RL 框架能串流更新權重，支援權重重新分佈
- **生態整合**：與 vLLM-TorchTPU、SGLang-TorchTPU 和 llm-d 等開源框架整合，支援 PyTorch 和 JAX 生態

## 結論
TPU Sync 透過開源庫形式提供高效能的 TPU 模型狀態層，解決分散式推理和強化學習中的記憶體瓶頸，已與多個開源框架合作並獲得前沿 AI 實驗室和企業的驗證。
---
