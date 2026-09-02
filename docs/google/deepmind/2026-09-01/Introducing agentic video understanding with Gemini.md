# Introducing Agentic Video Understanding with Gemini

- **來源**: Google DeepMind
- **發布日期**: 2026-09-01
- **原文連結**: https://deepmind.google/blog/introducing-agentic-video-in-gemini/

## 核心主題
Google DeepMind 正式推出「代理式影片理解」(Agentic Video Understanding) 功能，透過動態掃描影片片段，大幅提升影片分析準確度，同時大幅降低 Token 消耗與成本。

## 關鍵重點
- **效率提升**：Token 消耗減少高達 88%，成本降低高達 66%，準確度提升高達 7%
- **支援模型**：Gemini 3.7 Flash、3.6 Flash 和 3.5 Flash-Lite 模型
- **核心能力**：
  - 秒級時刻檢索 (sub-second moment retrieval)
  - 長影片針在 haystack 搜尋 (long-form needle-in-a-haystack search)
  - 異常檢測 (anomaly detection)
  - 動作與物件計數 (counting action & object)
- **技術原理**：取代靜態處理方式，採用代理式迴圈動態決定觀看速度與重點片段
- **使用方式**：在 Google AI Studio 或 Gemini Enterprise Agent Platform 中將 API 設定為 "agentic" 即可啟用

## 結論
此功能標誌著影片處理的重大突破，讓開發者能以更低成本處理長影片內容，同時獲得更高準確度。Gemini 3.7 Flash 在品質與成本效率上達到最佳平衡點，並將逐步滾動至 Google 產品群中。

---