# EmbeddingGemma 2: an open, lightweight multimodal embedding model

- **來源**: Google DeepMind
- **發布日期**: 2026-10-06
- **原文連結**: https://deepmind.google/blog/embeddinggemma-2-an-open-lightweight-multimodal-embedding-model/

## 核心主題
Google DeepMind 推出 EmbeddingGemma 2，這是首個原生支援多模態（文字、圖片、音訊、影片）的開源輕量型嵌入模型，可將多種媒體類型統一映射到單一嵌入空間，專為端側設備優化。

## 關鍵重點
- **最佳效能與輕量設計**：7.4 億參數的模型在 MTEB、MAEB 等 benchmarks 上表現優異，且可透過模組化設計僅需 2.7 億參數處理文字任務。
- **儲存效率提升**：採用 Matryoshka Representation Learning (MRL)，可將輸出向量從 768 維度動態縮減至 512/256/128 維度，節省高達 6 倍的儲存空間。
- **端側優化**：在 Google Pixel 11 Pro 上，文字僅需約 191MB RAM，完整多模態模型約 567MB RAM，支援 8K token 上下文（可處理 5.5 分鐘音訊或 29 張圖片）。
- **跨模態能力**：可根據文字查詢搜尋音訊記錄、從語音備忘錄定位影片片段，並支援本地代碼索引與語義代碼搜尋。
- **開源授權**：採用商業友好的 Apache 2.0 授權，可自由用於商業應用。

## 結論
EmbeddingGemma 2 代表多模態嵌入模型的重要突破，透過輕量化與端側優化，讓開發者能在本地硬體上實現隱私導向的跨模態搜尋與檢索系統，無需依賴雲端服務。
---
