# LFM2.5-Encoders for Fast Long-Context Inference on CPU

- **來源**: Hugging Face
- **發布日期**: 2026-07-28
- **原文連結**: https://huggingface.co/blog/LiquidAI/lfm2-5-encoders

## 核心主題
Liquid AI 推出了兩款 LFM2.5 編碼器模型，在長上下文推理上比傳統模型快 3.7 倍，即使運行在 CPU 上也能高效處理長文檔。

## 關鍵重點
- 推出了 LFM2.5-Encoder-230M 和 LFM2.5-Encoder-350M 兩款模型，支持 8,192 token 上下文
- 在 CPU 上比 ModernBERT-base 快 3.7 倍，適合長文檔分類、路由等任務
- 在 GLUE、SuperGLUE 等多語言任務上表現優異，甚至超越更大模型
- 提供零射線提示路由、政策檢查、拼寫檢查、PII 檢測等實時演示
- 可通過 transformers 庫輕鬆加載和微調，適合高頻次理解任務

## 結論
這些模型為需要低成本、快速處理長文檔的生產環境提供了理想的解決方案，特別適合在現有 CPU 硬件上運行。
---
