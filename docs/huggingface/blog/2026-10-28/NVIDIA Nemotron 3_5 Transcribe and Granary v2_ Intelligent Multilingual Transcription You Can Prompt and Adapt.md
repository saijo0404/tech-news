# NVIDIA Nemotron 3.5 Transcribe and Granary v2: Intelligent Multilingual Transcription You Can Prompt and Adapt

- **來源**: Hugging Face Blog
- **發布日期**: 2026-10-28
- **原文連結**: https://huggingface.co/blog/nvidia/nemotron-transcribe-granary

## 核心主題
NVIDIA Nemotron 3.5 Transcribe 與 Granary v2 是新一代多語言語音識別系統，整合語音轉文字、說話者歸屬、翻譯等功能，支援40種語言，並提供優異的排行榜表現與醫療場景優化。

## 關鍵重點
- **排行榜表現優異**：Hugging Face Open ASR Leaderboard 英語 WER 5.33%（第一），多語言平均 4.62% WER（最低），David AI diarization leaderboard 最低錯誤率，VoiceArena diarization benchmark 排名第一
- **醫療場景優化**：WER 從30.8%降至11.8%（比原始模型少62%錯誤），持外說話者測試 WER 降低45.8%，訓練成本僅需約14 GPU小時（單台NVIDIA GB300）
- **Granary v2 數據管道**：提供463,062小時跨48種語言的多語言語音數據，支援三種轉文字格式（原始、清洗版、逆轉文字正規化）
- **開發者工具與部署**：支援自然語言提示控制輸出、可調整輸出格式、可通過vLLM部署，支援RTX Spark、DGX Spark、Jetson AGX Thor等硬體

## 結論
NVIDIA Nemotron 3.5 Transcribe 與 Granary v2 在性能、多語言支援和醫療場景優化方面表現突出，是當前最先進的語音識別解決方案之一，適合醫療、多語言應用及邊緣設備部署。

---

檔案已成功儲存至指定路徑。