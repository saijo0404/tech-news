# Token Pooling-Aware Training for Multi-Vector Embedding Models

- **來源**: Hugging Face Blog
- **發布日期**: 2026-11-11
- **原文連結**: https://huggingface.co/blog/token-pooling

## 核心主題
這篇文章介紹了針對多向量嵌入模型的 Token Pooling 感知訓練方法，通過向量合併減少文件向量數量，同時優化原始嵌入和壓縮後嵌入。

## 關鍵重點
- **Token Pooling 技術**：使用 Ward 階層聚類將相似 token 向量合併，例如 pool_factor=4 時文件向量減少至 1/4
- **Pooling-Aware Training**：訓練時同時優化原始嵌入和壓縮後嵌入，損失函數為 L = 0.5 × L_unpooled + 0.5 × L_pooled
- **性能提升**：相同壓縮率下性能從 94.6% 提升至 97.8%，NanoBEIR@13 分數從 51.84 提升至 52.39
- **壓縮技術優先順序**：Embedding quantization (4/2/1 bit) > Token pooling > Matryoshka token embeddings
- **實現方式**：使用 Sentence Transformers 的 MultiVectorEncoder 和 MultiVectorTokenPoolingLoss 損失函數

## 結論
Token Pooling-Aware Training 方法在保持高性能的同時大幅減少向量儲存需求（74.8% 儲存減少），是優化多向量嵌入模型的有效策略，可與 LateOn 等模型搭配使用。
---