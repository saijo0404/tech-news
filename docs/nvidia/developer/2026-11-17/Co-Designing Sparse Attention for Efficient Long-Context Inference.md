# Co-Designing Sparse Attention for Efficient Long-Context Inference

- **來源**: developer.nvidia.com/blog
- **發布日期**: 2026-11-17
- **原文連結**: https://developer.nvidia.com/blog/co-designing-sparse-attention-for-efficient-long-context-inference/

## 核心主題
本文介紹 NVIDIA 如何協同設計稀疏注意力（Sparse Attention）以優化長上下文推理效能，透過八項設計準則大幅降低計算成本。

## 關鍵重點
- **稀疏注意力架構**：每個查詢僅關注少量關鍵字，將注意力成本轉移至索引器（Indexer）階段，降低長上下文推理負擔。
- **索引器設計關鍵**：KH=1 並跨頭減除、頭維數 Hsz 建議 128 或 256、索引器尾部和累加使用 FP16 提升吞吐量。
- **效能優化策略**：保持 G x (D+1) 在單一 Tensor Core tile（約 200 行）內，透過 Top-k 選取融合加速 2.1x-2.4x。
- **八項設計準則**：Top-k 優化、Block-level 選擇粒度、Head 共享、Tensor Core 優化、記憶體與效能優化，可大幅降低稀疏模型在 NVIDIA GPU 上的長上下文成本。

## 結論
透過 NVIDIA 協同設計的稀疏注意力架構與八項優化準則，可在 128K 上下文下顯著降低注意力計算成本，適用於 DeepSeek V3.2、GLM 5.2/5.3、Qwen QSA 等模型，大幅提升長上下文推理效能。

---