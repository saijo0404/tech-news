# Rumble-2-Flash: an open 0.5B speech model for 40+ languages

- **來源**: Hugging Face Blog
- **發布日期**: 2026-11-18
- **原文連結**: https://huggingface.co/blog/rumble-2-flash

## 核心主題
Reson8 推出了一個 0.5B 參數的開放源碼語音識別模型，支援 40 多種語言，性能媲美 3-60 倍大小的模型。

## 關鍵重點
- **極速處理**：一小時音訊只需約 0.5 秒，每秒處理超過 7000 RTF，在完整批次下表現卓越
- **多語言支援**：支援 40+ 種語言並具備自動語言檢測功能，涵蓋中文、德語、法語等多種語言
- **電話語音識別**：在 AppTek 呼叫中心測試中達到 7.86% WER，與 NVIDIA 30B 模型相當，優於同系列 Qwen3-ASR 0.6B 模型
- **開放源碼**：採用 Apache 2.0 授權，原生支援 🤗 Transformers 和 vLLM，無需額外代碼
- **訓練方法**：使用 Qwen3-ASR 架構，透過 on-policy distillation 技術訓練，學生模型直接從音訊學習並獲得即時反饋

## 結論
Rumble-2-Flash 是一個在性能、速度和多語言支援方面都表現優異的小型語音識別模型，特別適合需要快速處理、多語言支持和低成本部署的應用場景。

---