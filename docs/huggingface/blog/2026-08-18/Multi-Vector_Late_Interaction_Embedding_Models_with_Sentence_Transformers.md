# Multi-Vector Late Interaction Embedding Models with Sentence Transformers

- **來源**: Hugging Face Blog
- **發布日期**: 2026-08-18
- **原文連結**: https://huggingface.co/blog/multi-vector-encoder

## 核心主題
本文介紹了 Sentence Transformers 中的 MultiVectorEncoder 模型（LateOn/ColBERT）在語義搜尋中的應用，支援多向量檢索與多模態能力。

## 關鍵重點
- **Multi-Vector 模型**：每個 token 保留獨立向量（而非壓縮成單一向量），類似 ColBERT 的 late interaction 檢索方式
- **MaxSim 運算子**：查詢時對每個查詢 token 取與文件 token 的最高相似度，保留 token 層級資訊
- **檢索品質提升**：特別適合多條件查詢（如「綠色沙發配木腿」）和跨領域數據
- **索引大小增加**：約 42 倍於 MiniLM 索引（62 KiB/篇），需透過 Token Pooling、Retrieve and Rerank 等優化方案
- **多模態檢索能力**：支援文本、圖像、音頻、視頻等多模態輸入，ColPali 系列模型專用於視覺文檔檢索
- **向量資料庫支援**：支援 Qdrant (v1.10+), Weaviate (v1.29+), Vespa, LanceDB (v0.15.0+), Milvus (v2.6.4+) 等
- **性能優化**：HierarchicalTokenPooling 可大幅減少索引佔用空間，GPU 上使用 fp16 + Flash Attention 可達 2.44 倍速度提升
- **訓練指南**：提供完整的訓練腳本、評估工具（NanoBEIR）及多模態模型訓練方法

## 結論
MultiVectorEncoder 提供了更精確的語義檢索能力，特別適合需要保留 token 層級資訊的應用場景，但需權衡索引大小和計算成本。透過適當的優化方案（如 Token Pooling、向量資料庫加速），可在性能與資源之間取得平衡。

---