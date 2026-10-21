# AnyLanguageModel 1.0: One Year of Local Models on Apple Platforms

- **來源**: Hugging Face
- **發布日期**: 2026-10-20
- **原文連結**: https://huggingface.co/blog/anylanguagemodel-1-0

## 核心主題
Hugging Face 推出 AnyLanguageModel 1.0，提供統一 API 讓開發者可以在 Apple 平台上選擇本地或雲端模型，解決了開發者對本地模型不熟悉的問題。

## 關鍵重點
- **統一 API 設計**：只需將 import 語句從 FoundationModels 改為 AnyLanguageModel，即可使用系統模型、本地模型（llama.cpp、MLX、Core ML）或雲端服務
- **功能全面增強**：工具調用、引導生成、圖片輸入等功能已支援所有提供者，包括嵌套 @Generable 類型和陣列
- **雲端模型支援擴大**：新增支援 OpenAI、Anthropic、Google Gemini、Ollama、Hugging Face Inference Providers 等雲端服務
- **本地模型能力提升**：Gemma 4 E2B（3.4GB）、LFM2.5 2.6B（1.7GB）、Qwen3.8 27B（16GB）等模型更強大，部分可運行於 iPhone
- **swift-huggingface 與 swift-xet 1.0**：加速模型下載，提升開發體驗

## 結論
AnyLanguageModel 1.0 透過統一 API 設計，大幅降低了在 Apple 平台上使用本地或雲端模型的門檻，讓開發者可以更輕鬆地根據需求選擇合適的模型，推動了 Apple 生態系中本地 AI 模型的普及。
---