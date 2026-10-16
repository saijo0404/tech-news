# Granite Switch 4.1: Chat, Decisions, and Speech from One Endpoint

- **來源**: Hugging Face
- **發布日期**: 2026-10-15
- **原文連結**: https://huggingface.co/blog/ibm-granite/granite-switch-4-1

## 核心主題
Granite Switch 4.1 模型整合了決策適配器和最快的語音識別模型，允許在同一端點上高效切換自然語言回應、決策和語音轉文字任務。

## 關鍵重點
- 整合了 Decision aLoRA（通用決策）、Guardian aLoRA（安全決策）和 Granite-Speech-5.0-Turbo-CTC（最快 ASR 模型）三種技術
- 所有技術共享同一個 KV cache，使模型在 GPU 上佔用的 VRAM 與基礎模型相同，實現更多功能以較少 GPU
- 使用 Activated LoRAs 技術，可以快速切換不同任務，並支援自訂適配器的組建

## 結論
Granite Switch 4.1 展示了模組化 AI 模型的強大潛力，允許開發者通過組合不同適配器來創建專用的 AI 解決方案，同時保持高效和靈活性。
---
