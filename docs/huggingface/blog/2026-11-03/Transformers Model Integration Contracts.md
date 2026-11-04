# Transformers Model Integration Contracts

- **來源**: Hugging Face Blog
- **發布日期**: 2026-11-03
- **原文連結**: https://huggingface.co/blog/transformers-mic

## 核心主題
Hugging Face 推出 Model Integration Contracts (MIC) 標準，透過縮小模型建立測試 fixture，在 PR 階段就能快速捕捉回歸錯誤，避免大規模 GPU 測試的昂貴與延遲。

## 關鍵重點
- **為什麼錯誤會進入 main**：Transformers 支援 750+ 模型類型，每日執行 20 萬+ GPU 測試，但全量測試不具可行性。錯誤往往在合併後才被發現。
- **Model Integration Contract (MIC) 架構**：包含三個部分：Fixture（縮小模型）、Usage Path（使用範例）、Baselines（基準輸出）。合約成立需驗證使用範例輸出與基準一致。
- **UMT5 回歸案例**：2026 年 7 月 30 日引入的 SDPA 注意力機制導致 UMT5 訓練時能看見未來 token。小型 UMT5 fixture（66MB）成功捕捉到該錯誤，而完整模型（1.227GB）則無法在 PR 階段發現。
- **模型縮小四步驟**：1) 縮小配置（保留層類型）2) 保持預處理不變 3) 驗證權重（隨機或過擬）4) 凍結記錄。Llama 4 Scout 案例：1086 億參數縮減至 4470 萬。
- **隨機 vs 過擬權重**：隨機權重 fixture 捕捉 18/24 個注入錯誤，過擬 fixture 捕捉 24/24 個。但兩者都錯過了一個輔助解碼錯誤。
- **tmic CLI 工具**：自動化生成 MIC，LLM 撰寫使用代碼，人工審查後才上線。

## 結論
Model Integration Contracts 提供了一種實用且低成本的測試策略，能在 PR 階段快速發現回歸問題，雖然目前不阻塞合併，但已證明能有效捕捉錯誤。未來希望將原始 Hub 模型頁面與 MIC 連結，形成完整的測試生態。

---