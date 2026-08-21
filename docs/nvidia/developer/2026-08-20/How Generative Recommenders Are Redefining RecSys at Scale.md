# How Generative Recommenders Are Redefining RecSys at Scale

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-08-20
- **原文連結**: https://developer.nvidia.com/blog/how-generative-recommenders-are-redefining-recsys-at-scale/

## 核心主題
本文介紹了推薦系統（RecSys）如何從傳統基於嵌入的架構轉向生成式推薦（Generative Recommenders, GRs），利用序列建模目標和類 Transformer 架構來解決可擴展性、冷啟動和長尾問題。NVIDIA 提供了 `recsys-examples` 和 `nv-embedding-cache` 等工具來支持這一轉變。

## 關鍵重點
- **生成式推薦架構**：HSTU（Hierarchical Sequential Transduction Units）和 Semantic IDs 是兩種主流的生成式推薦架構，將推薦問題重新表述為類似 LLM 的序列預測問題。
- **recsys-examples 倉庫**：提供基於 NVIDIA GPU 的生產級實現，包括 DynamicEmb（動態嵌入表）、優化過的 KV Cache、融合 CUDA 核以及 Megatron-Core 和 TorchRec 的並行支持。
- **nv-embedding-cache (NVE)**：提供分層多級緩存解決方案，支持海量嵌入表的無縫分片和並發查找/淘汰，實現低延遲推理和高吞吐量。

## 結論
生成式推薦系統通過利用 LLM 生態系統和序列建模優勢，正在重新定義大規模推薦系統。NVIDIA 通過提供生產級工具和優化架構，幫助開發者克服傳統推薦系統在可擴展性、冷啟動和長尾問題上的挑戰，同時滿足嚴格的低延遲要求。

---