# Welcome Inkling 2 Mini, Cutting-edge Performance for your Local Setup

- **來源**: Hugging Face
- **發布日期**: 2026-11-20
- **原文連結**: https://huggingface.co/blog/inkling2mini

## 核心主題
Inkling 2 Mini 是一款專為本地 AI 設備設計的混合專家模型，透過循環機制提升性能，在 AA v5 指數中領先 32 項測試。

## 關鍵重點
- **模型架構**：混合專家模型 (MoE)，約 26B 物理參數，每 token 3B 活躍參數，24 解碼器層其中 12 層中間層循環執行 3 次
- **多模態能力**：支援圖片與文字輸入，可進行圖片描述、3D 場景生成，從草圖轉化為完整應用程式
- **性能表現**：在 AA v5 指數中領先，48 項測試中領先 32 項，優於 Gemma 4 31B、Muse Glimmer、Qwen3.8-27B 等模型
- **推理支援**：支援 transformers、Llama App、MLX、SGLang 等多個框架，提供 GGUF 4-bit (IQ4_NL) 與 8-bit (Q8_0) 量化版本
- **本地部署優勢**：體積小於 Inkling 2 Small，可調整循環次數 (1-3 次) 平衡速度與品質，支援 DSpark 猜測解碼加速

## 結論
Inkling 2 Mini 是本地 AI 設備的理想選擇，提供卓越的性能與靈活性，特別適合需要多模態能力和程式碼生成的場景。

---
