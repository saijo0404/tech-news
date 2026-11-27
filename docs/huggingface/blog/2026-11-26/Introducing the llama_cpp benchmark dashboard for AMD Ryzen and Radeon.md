# Introducing the llama.cpp benchmark dashboard for AMD Ryzen and Radeon

- **來源**: Hugging Face
- **發布日期**: 2026-11-26
- **原文連結**: https://huggingface.co/blog/ggml-org/llamacpp-amd-bench

## 核心主題
介紹了一個在 Hugging Face 上可用的 llama.cpp × AMD 比對儀表板，讓開發者可以追蹤在 AMD Ryzen 和 Radeon 硬體上的本地推理表現。

## 關鍵重點
- 儀表板提供 Radeon 8060S (gfx1151) 和 Radeon AI Pro R9700S (gfx1201) 兩種硬體選擇，可比較不同量化版本的表現。
- 提供 PP512（處理512個輸入 token）和 TG128（生成128個 token）兩種測試工作負載，以 tokens/秒為單位衡量性能。
- 比對儀表板使用公開數據，來自 ggml-org/install.sh-benches-data 儲存桶，並每週自動更新。
- 支援多種模型（Inkling 2 Mini、Qwen、Gemma、gpt-oss、LFM）和 GGUF 格式（Q4_K_M、Q8_0、BF16、F16 等）。
- 感謝 AMD 團隊提供測試基礎設施並協助驗證設定。

## 結論
這個比對儀表板為 AMD 開發者提供了追蹤本地 AI 推理性能演變的透明工具，並鼓勵社區分享更多模型和工作負載的需求。
---
