# Welcome Inkling by Thinking Machines

- **來源**: Hugging Face
- **發布日期**: 2026-07-15
- **原文連結**: https://huggingface.co/blog/thinkingmachines-inkling

## 核心主題
Thinking Machines 推出了 Inkling 1T 參數多模態語言模型，結合 1M tokens 上下文窗口與混合專家架構，在視覺推理、音訊理解及工具使用上展現卓越表現。

## 關鍵重點
- **多模態能力**：原生支援圖像、文字、音頻輸入，具備 OCR、邏輯推理及多語言理解能力
- **硬體優化**：透過 NVFP4 量化仅需 600GB VRAM，或 Unsloth 1-bit 量化可將 VRAM 需求減少 95%
- **推理優化**：採用短 1D 卷積（SConv）加速推理，支援 transformers、SGLang、vLLM、llama.cpp 等多種引擎
- **測試表現**：視覺推理任務中難度 1,000+ 題全數通過，音訊理解 VoiceBench 達 91.4%
- **工具使用**：MCP Atlas 74.1%、Terminal Bench 2.1 63.8，支援 ECHO 與 GOLD 演算法進行後訓練

## 結論
Inkling 模型展現了多模態推理與工具使用能力的重大突破，透過高效能架構設計與量化技術，為開發者提供了更便捷的部署方案，特別適合需要處理複雜視覺與音訊任務的應用場景。
---

檔案已成功儲存至指定路徑。
