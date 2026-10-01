# Open TTS Leaderboard: Scalable Evaluation for Multilingual Text-to-Speech and Voice Cloning

- **來源**: Hugging Face Blog
- **發布日期**: 2026-09-30
- **原文連結**: https://huggingface.co/blog/open-tts-leaderboard

## 核心主題
Hugging Face 推出新的 Open TTS Leaderboard，使用客觀指標評估多語言 TTS 模型，解決現有排行榜無法跟上開放源碼模型發布速度的問題。

## 關鍵重點
- **客觀指標取代主觀評分**：使用 WER/CER（可懂度）、RTFx/TTFA（速度）、Speaker Similarity（語音相似度）等客觀指標，評估時間從數週縮短至數小時
- **多語言與語音克隆支援**：支援多語言評估（包括中文、日文、韓文等），並提供語音克隆功能，可比較不同模型在特定語音特徵上的表現
- **社群互動功能**：提供「Listen」和「Streaming」功能，讓使用者可以聆聽比較並投票，甚至可將投票數據納入排行榜
- **專注開放源碼模型**：針對常被忽略的開放源碼 TTS 模型進行評估，並計劃開放評估腳本供社群使用

## 結論
此排行榜旨在由社群共同塑造，以確保評估持續相關且具洞察力。透過開放評估腳本和社群回饋機制，Hugging Face 希望與開發者共同推動 TTS 評估標準的進步。
---