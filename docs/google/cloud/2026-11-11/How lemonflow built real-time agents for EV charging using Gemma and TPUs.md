# How lemonflow built real-time agents for EV charging using Gemma and TPUs

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-12
- **原文連結**: https://cloud.google.com/blog/topics/startups/building-real-time-agents-for-ev-charging-using-gemma-and-tpus/

## 核心主題
lemonflow 使用 Google Cloud TPU 自部署 Gemma 4 模型，建立低延遲的實時 AI 代理系統，解決電動車充電失敗問題。

## 關鍵重點
- 將管理 API 遷移至自部署 Gemma 4 模型於 Google Cloud TPU v6e 硬體，實現 P50 延遲約 350 毫秒，P90 延遲約 600 毫秒，比管理 API 快三倍
- 支援超過 40 個充電網絡、17 個國家、25 萬個充電站，每 90 秒就有一位 EV 駕駛獲得協助
- 建立 Agent Coach 背景引擎，將實際對話轉化為測試案例，並導入 nightly 自動化回歸測試
- 支援 90 種語言，99.9% 的即時對話回合由 Gemma 回答，並具備自動 fallback 機制
- 透過標準化翻譯層整合 30 個不同的 Charge Point Management Systems (CPMS)，解決後端碎片化問題

## 結論
透過自部署開源模型與專用 TPU 硬體，lemonflow 實現了低延遲、高可靠性的電動車充電支援系統，目標是讓駕駛者不再被困在充電站。

---