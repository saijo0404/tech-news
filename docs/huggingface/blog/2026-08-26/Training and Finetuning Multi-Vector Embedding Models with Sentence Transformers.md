# Training and Finetuning Multi-Vector Embedding Models with Sentence Transformers

- **來源**: Hugging Face Blog
- **發布日期**: 2026-08-26
- **原文連結**: https://huggingface.co/blog/train-multi-vector-encoder

## 核心主題
這篇文章介紹如何使用 Sentence Transformers 訓練多向量嵌入模型，並展示在醫療領域的優異表現。

## 關鍵重點
- **多向量模型優勢**：與單向量模型不同，保留每個 token 的獨立向量，使用 MaxSim 操作符進行查詢與文檔評分，檢索表現更強但索引體積較大
- **訓練效率**：14.5 小時內，單張 RTX 3090 即可訓練完成；10 萬樣本訓練可在 75 分鐘內達到與 100 萬樣本相近效果
- **醫療領域表現**：mLateOn-medical 模型在 MIRIAD 測試集上取得 NDCG@10 = 0.9139，超越所有零射模型
- **索引優化策略**：1-bit PLAID 量化 + 剪枝，壓縮比達 13 倍，NDCG@10 僅下降 0.0155；極端壓縮下保留 10% 向量仍達 0.8765
- **技術特性**：支持長文檔（8192 token 上下文）、可配置文檔長度、標點符號跳過列表等參數

## 結論
多向量嵌入模型訓練在特定領域（如醫療）能顯著提升檢索表現，通過量化和剪枝等優化策略可大幅降低索引大小，實現性能與效率的最佳平衡。

---