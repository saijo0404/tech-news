# Featuring Every Eval Ever Results on Hugging Face Model Pages

- **來源**: Hugging Face Blog
- **發布日期**: 2026-06-30
- **原文連結**: https://huggingface.co/blog/eee-community-evals

## 核心主題
Hugging Face 與 **Every Eval Ever**（EEE）達成整合，將分散在論文、排行榜、博客與 harness 日誌中的模型評估結果統一至 Hugging Face 模型頁面，讓每個評估分數都回溯至結構化的完整記錄，解決評估數據散落、難以比較的痛點。

## 關鍵重點
- **評估數據的碎片化問題**：同一模型在同一基準上的分數因評估者不同而差異巨大——例如 LLaMA 65B 在 MMLU 上被報告為 **63.7** 與 **48.8** 兩種結果，差距來自未報告的評估設定（prompt 方式、generation 參數、harness 版本等）。EEE 提出單一 **JSON Schema** 統一記錄評估結果的完整元數據：誰跑的、哪個模型、存取方式、生成設定、指標含義，以及可選的 JSONL 樣本輸出檔案。EEE 資料儲存庫已累積 **22.9 萬筆**評估結果，涵蓋 2.2 萬個模型與 2,200 個基準。
- **雙向整合：模型頁面顯示 + EEE 全記錄回溯**：將 EEE 結果提交至 Hugging Face 後，分數會出現在模型卡片上並納入該基準的排行榜；同時每個分數帶有 **Source EvalEval 徽章**，連結至包含生成配置、harness 版本、可複現性說明等完整資訊的 EEE JSON 記錄。兩方各司其職——Hugging Face 把結果放在人會看模型的地方，EEE 保留可解釋的結構化記錄並驅動 Eval Cards。
- **自動轉換工具與流程**：Hugging Face 提供 **Community Evals Converter**，將 EEE JSON 記錄轉換為 Hugging Face 的 YAML 格式（目前支援 MMLU-Pro、GPQA、HLE、GSM8K 四個基準）。工具會自動校驗資料雜湊、稽核現有結果、標記衝突或重複，且在推送前產生本地預覽與審閱報告——必須手動輸入 `OPEN PRS` 才會提交，全程無自動化推送，確保貢獻者完全掌控。

## 結論
EEE 與 Hugging Face Community Evals 的整合，將模型評估從「散落各處的數字」升級為「可追溯、可解釋、可比較」的標準化基礎設施。開發者只需多一個步驟提交 EEE 記錄，轉換器就會自動將結果同步至模型頁面並附帶完整回溯鏈——讓研究人員、政策制定者與使用者在選擇模型時，能真正信任和理解那些分數背後的意義。

---
