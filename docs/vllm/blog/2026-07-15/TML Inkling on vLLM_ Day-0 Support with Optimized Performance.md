# TML Inkling on vLLM: Day-0 Support with Optimized Performance

- **來源**: vLLM Blog
- **發布日期**: 2026-07-15
- **原文連結**: https://vllm.ai/blog/2026-07-15-inkling

## 核心主題
vLLM 正式支援 TML Inkling 模型，提供完整的 Day-0 支援與優化性能，支援多模態輸入與 1M 上下文長度。

## 關鍵重點
- 支援兩個模型版本：thinkingmachines/Inkling-NVFP4 和 thinkingmachines/Inkling (BF16)
- 原生支援文字、圖片、音訊輸入，並可生成文本，上下文長度最高可達 1M tokens
- 在 4 台 GB200 GPU 上達到最高 380 tok/s/user（使用 MTP）的性能，無 MTP 時為 140 tok/s/user
- 完整功能對齊：LoRA、TP/DP/EP/PP 並行、前綴快取、分散式服務等
- 包含 Sconv 感知的 TP 分割、低延遲合併集合等優化，解決相對注意力機制帶來的記憶體存取問題

## 結論
vLLM 成功整合 TML Inkling 模型，通過一系列優化實現卓越性能，並在全面測試中驗證了準確性。未來將進一步支援 FP8 全球注意力、CUDA 圖表及 AMD GPU 支援。
---
