# EmbeddingGemma 2: an open, lightweight multimodal embedding model

- **來源**: Google Blog
- **發布日期**: 2026-10-06
- **原文連結**: https://blog.google/innovation-and-ai/technology/developers-tools/embeddinggemma-2/

## 核心主題
Google DeepMind 推出 EmbeddingGemma 2，這是首款原生支援多模態（文字、圖片、音頻、影片）的開源輕量型嵌入模型，可運行於端裝置上。

## 關鍵重點
- **7.4 億參數的輕量模型**：支援文字、程式碼、圖片、影片和音頻的统一嵌入空間，在 MTEB Code 和 MAEB 等 benchmarks 上表現優異
- **端裝置優化**：在 Google Pixel 11 Pro 上，文字僅需約 191MB RAM，完整多模態模型約需 567MB RAM
- **8K token 上下文窗口**：可處理 5.5 分鐘音頻、29 張圖片或 58 個影片幀
- **程式碼表現提升**：MTEB Code 表現從 68.76 提升至 78.68，提升 9.92 分
- **儲存效率優化**：透過 Matryoshka Representation Learning (MRL)，可將向量維度從 768 降至 128，節省 6 倍儲存空間
- **Apache 2.0 開源許可**：商業友好，可自由使用與分發

## 結論
EmbeddingGemma 2 是端裝置多模態嵌入模型的突破，為開發者提供隱私優先、低資源消耗的跨模態搜尋與檢索解決方案，並可與 Gemma 4 搭配構建完整的端裝置 RAG 系統。
---
