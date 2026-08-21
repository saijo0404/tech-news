# Up to 3.2x Faster Inference with LFM2.5-DSpark

- **來源**: Hugging Face
- **發布日期**: 2026-08-20
- **原文連結**: https://huggingface.co/blog/LiquidAI/lfm25-dspark

## 核心主題
LiquidAI 推出了 LFM2.5-DSpark 系列模型，通過 speculative decoding 技術實現推理速度提升，最高達 3.18 倍（GPU）和 2.87 倍（端上設備），同時保持輸出品質不變。

## 關鍵重點
- 推出了三個 LFM2.5 系列模型的 DSpark draft 模型檢查點：LFM2.5-1.2B-Instruct、LFM2.5-2.6B 和 LFM2.5-8B-A1B
- DSpark 技術結合了 DFlash 風格的並行 backbone、輕量級 Markov chain 頭部和信心調度的驗證器
- 在 H100 GPU 上最高達 3.18 倍速度提升，在 M4 Max MacBook 上達 2.27 倍速度提升
- 支持 llama.cpp 和 SGLang 的 Day-one 集成，已開源 upstream
- LFM2.5-2.6B 模型在端上設備上平均減少 57% 的函數調用延遲

## 結論
LFM2.5-DSpark 系列模型通過輕量級的 draft 模型實現推理加速，為邊緣設備和雲端部署都帶來顯著的性能提升，同時保持與基準模型相同的輸出品質。
---