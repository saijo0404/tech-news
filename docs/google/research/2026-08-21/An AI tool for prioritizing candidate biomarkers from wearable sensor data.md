# An AI tool for prioritizing candidate biomarkers from wearable sensor data

- **來源**: Google Research Blog
- **發布日期**: 2026-08-21
- **原文連結**: https://research.google/blog/an-ai-tool-for-prioritizing-candidate-biomarkers-from-wearable-sensor-data/

## 核心主題
Google Research 推出 Biomarker Discovery Framework，一個多代理 AI 系統，用於從可穿戴設備感測器數據中發現生物標本候選者，透過迭代假設生成、統計分析和文獻驗證提升臨床研究效率。

## 關鍵重點
- **多代理協作架構**：系統整合 Orchestrator 協調器與多個專責代理（Scout、Critic、Defender 等），執行六階段閉環流程，從數據理解到報告撰寫。
- **統計嚴謹性保障**：透過對抗驗證機制（11 項檢查）與特徵建構與目標信號分離，避免假相關、資料洩漏與過度擬合問題。
- **跨群體驗證成果**：在三個大型群體（共 9,279 名參與者觀察）中，成功識別 41 個心理健康候選生物標本與 25 個代謝結果候選，並提升預測效能。
- **人類監督機制**：所有分析結果需經專家審查，確保統計有效性與臨床意義，避免黑盒自動化帶來的風險。

## 結論
Biomarker Discovery Framework 證明 AI 系統在結構化架構下，能有效加速生物標本發現過程，同時維持統計嚴謹性與人類監督，為臨床研究提供可信任的自動化輔助工具。

---