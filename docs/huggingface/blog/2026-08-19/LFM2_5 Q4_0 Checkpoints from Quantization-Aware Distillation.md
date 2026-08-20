# LFM2.5 Q4_0 Checkpoints from Quantization-Aware Distillation

- **來源**: Hugging Face
- **發布日期**: 2026-08-19
- **原文連結**: https://huggingface.co/blog/LiquidAI/qad

## 核心主題
Liquid AI 推出了經過量化感知精煉（QAD）技術訓練的 LFM2.5 模型 4-bit 檢查點，在保持低記憶體佔用和高吞吐量的同時，恢復了 97% 的量化精度損失。

## 關鍵重點
- 推出了四款 LFM2.5 模型的 Q4_0 GGUF 檢查點：LFM2.5-230M、LFM2.5-350M、LFM2.5-1.2B-Instruct 和 LFM2.5-2.6B
- 採用量化感知精煉（QAD）技術，將高精度教師模型精煉到量化學生模型，恢復了 97% 的量化精度損失
- 在邊緣硬體上表現優異：230M 和 350M 模型在 Q5_K_M 質量下擁有 4-33% 更高的解碼吞吐量，1.2B 和 2.6B 模型在 Q4_K_M 質量下擁有 3-14% 更高的吞吐量
- 可在 llama.cpp 或其他支持 GGUF Q4_0 的運行時中使用

## 結論
這些 QAD GGUF 檢查點使開發者能夠在邊緣設備上運行 LFM2.5 模型，同時保持高品質和低資源消耗。
---
