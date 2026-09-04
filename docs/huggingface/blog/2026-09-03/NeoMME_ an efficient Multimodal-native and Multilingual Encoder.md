# NeoMME - an efficient Multimodal-native and Multilingual Encoder

- **來源**: Hugging Face Blog
- **發布日期**: 2026-09-03
- **原文連結**: https://huggingface.co/blog/Hcompany/neomme

## 核心主題
NeoMME 是一組高效的多語言多模態編碼器，整合原始影像與文字處理能力，支援多語言與長上下文，無需預訓練視覺塔即可達到優異性能。

## 關鍵重點
- 提供 260M 和 800M 參數的多語言多模態編碼器，不依賴預訓練視覺塔或因果語言模型
- 單一雙向 Transformer 架構同時處理文字 token 和原始圖片 patch，支援動態圖片解析度與長上下文（16,384 tokens）
- 性能優異：NeoMME -Retriever-260M nDCG@10 = 0.523，NeoMME -Retriever-800M nDCG@10 = 0.556，比同級模型使用更少參數
- 儲存優化：層級 token 池化 + 非對稱量化，儲存從 1.5 MB 降至 6 kB/頁（255 倍壓縮），保留 >95% 基準品質
- 推理速度快：260M 模型在 NVIDIA L40S 上每秒可編碼約 51 頁，比 ColModernVBERT 快一倍
- 支援 Apache 2.0 授權，可在 Hugging Face Transformers 使用，適用於視覺文件檢索和視覺 RAG 系統

## 結論
NeoMME 提供高效、輕量且多語言的多模態編碼解決方案，特別適合視覺文件檢索和視覺 RAG 系統，在性能、效率和儲存方面取得良好平衡。
---