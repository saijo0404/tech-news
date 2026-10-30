# Introducing AnySpeechRecognizer and AnyDecisionModel: Open Models for Speech and Decisions on Apple Platforms

- **來源**: Hugging Face
- **發布日期**: 2026-10-29
- **原文連結**: https://huggingface.co/blog/anydecisionmodel

## 核心主題
Hugging Face 推出兩個 Swift 套件 AnySpeechRecognizer 和 AnyDecisionModel，分別提供語音識別和決策模型，可選擇 NVIDIA、Alibaba 等開源模型在 Apple 平台運行。

## 關鍵重點
- **AnySpeechRecognizer**：支援 Parakeet、Qwen3-ASR 等多個語音識別引擎，並新增 Speaker diarization 功能以追蹤誰在說話
- **AnyDecisionModel**：提供類型安全的決策 API，可回答是/否、多選題和評分問題，返回概率和置信度而非生成文字
- **跨平台支援**：兩個套件都支援從 Hugging Face Hub 下載開源模型並在設備上運行，支援 MLX、Core AI、llama.cpp 等多個後端
- **性能優勢**：相比 Apple 原生框架，提供更多模型選擇，語音識別速度快（Parakeet 可將一小時音頻轉寫為 20-40 秒）

## 結論
這兩個套件為開發者提供了更靈活、更輕量級的替代方案，相比 Apple 原生框架提供更多模型選擇，同時保持熟悉的 Swift API 體驗，特別適合需要處理語音識別和決策類型的應用場景。
---
