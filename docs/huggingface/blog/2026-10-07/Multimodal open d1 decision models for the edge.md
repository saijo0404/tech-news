# Multimodal open d1 decision models for the edge

- **來源**: Hugging Face Blog
- **發布日期**: 2026-10-07
- **原文連結**: https://huggingface.co/blog/LiquidAI/open-d1

## 核心主題
Liquid AI 於 2026 年 10 月 7 日發布兩款開放式決策模型，專為邊緣設備優化，在 NVIDIA Jetson AGX Thor 上僅需 16ms 即可回答問題。

## 關鍵重點
- **d1-3B 模型**：決策指數 48.57，支援文字與圖片輸入，在 NVIDIA Jetson AGX Thor 上推理速度僅需 16ms，基於 LFM2.5-VL-3B 訓練
- **d1-omni-600M 實驗性模型**：支援文字+圖片或文字+聲音輸入，決策指數 78.4，參數僅為 Decider 2B 的四分之一，基於 LFM2.5-Encoder-350M 訓練
- **核心優勢**：決策模型不產生 token，單次前向傳遞即可回答，在七個公開數據集上表現優異（平均分 82.9）
- **使用方式**：需安裝 transformers>=5.14，透過 transformers 載入模型，支援系統化問題解答與多模態輸入

## 結論
這些開放式決策模型為邊緣設備上的多模態推理提供了高效解決方案，特別適合資源受限環境下的快速決策應用。

---