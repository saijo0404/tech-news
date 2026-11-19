# 180B Parameters, 32GB of RAM: Pushing MoE Inference to the Limit with Transformers

- **來源**: Hugging Face Blog
- **發布日期**: 2026-11-18
- **原文連結**: https://huggingface.co/blog/moe-expert-streaming

## 核心主題
作者透過自訂的 Transformers 實現，將 MoE 專家直接從 SSD 串流至 GPU，在消費級硬體上接近 Strata 引擎的效能。

## 關鍵重點
- 將專家串流實現整合到 Transformers 的 from_pretrained 中，使用 experts_offload 參數，支援將專家權重從磁碟串流至 GPU
- 專家權重量化為 3 位數（49GB），n-gram 表保留在磁碟，僅串流路由選中的專家，大幅降低記憶體佔用
- 透過 Metal 核核、早期 GPU 提交、大區塊預填充和 LRU 串流策略，將效能提升至接近 Strata 的 14 tok/s

## 結論
雖然仍比 Strata 慢約 6%，但此方法證明了在消費級硬體上運行大型 MoE 模型的可行性，並提供了可移植的開源解決方案。所有 Metal 核核已發布在 Hugging Face Hub，歡迎回饋。

---