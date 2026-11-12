# Gemini Decisions API: Fast, calibrated multimodal decisions

- **來源**: Google Blog
- **發布日期**: 2026-11-11
- **原文連結**: https://blog.google/innovation-and-ai/technology/developers-tools/gemini-decisions-api/

## 核心主題
Google 推出 Gemini Decisions API，基於全新的 Gemini Decision 1 模型，提供快速、經過校準的多模態決策能力，可在單次請求中評估大量是/否、選擇題和評分問題。

## 關鍵重點
- **多模態支持**：支援文本、圖像、音頻、視頻和 PDF 等多種模態，可結合多種模態進行單一輸入
- **高效決策**：可在單次請求中評估高達 1,000 個獨立問題，端到端延遲僅 150-250 毫秒
- **成本優勢**：每 100 萬輸入令牌 0.10 美元，且無輸出令牌費用，比 Gemini 3.5 Flash-Lite 便宜近 5 倍
- **置信度評分**：每個答案都包含 0 到 1 的置信度分數，可將不確定情況路由到備用或人工審查員
- **三種決策類型**：支援 is/否判斷、多項選擇和評分（按順序評分）

## 結論
Gemini Decisions API 為開發者提供了快速、低成本且高準確性的多模態決策工具，特別適合工具選擇、政策檢查、模型路由和上下文評分等場景。開發者可以通過 Google AI Studio 獲取 API 鑰匙開始構建，並可參考 Python、JavaScript 和 REST 指南進行開發。

---
