# tokenizers v1: encode, decode and scaling, measured

- **來源**: Hugging Face
- **發布日期**: 2026-09-21
- **原文連結**: https://huggingface.co/blog/tokenizers-v1

## 核心主題
Hugging Face 推出 tokenizers v1，大幅優化編碼與解碼性能，比 v0.23 快 3 到 30 倍，解決 tokenizer 成為 ML 工作流瓶頸的問題。

## 關鍵重點
- **Bitcannon 替換正規表達式**：使用位元流操作與 SIMD 指令替代 regex 引擎進行分詞，大幅提升速度。
- **Word Cache 機制**：對重複詞彙建立本地快取，避免重複編碼，減少無效計算。
- **Merge Loop 重寫**：利用呼叫者專屬緩衝區，避免頻繁記憶體分配，提升 merge 效率。
- **多線程並行支援**：支援多工編碼，GPU 不再等待 CPU 完成 tokenization，提升整體吞吐量。

## 結論
tokenizers v1 保持 API 與輸出一致，性能大幅提升，已發布為 release candidate 供開發者測試。後續將擴展更多模型支援並優化 transformers 生態系。
---
