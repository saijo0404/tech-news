# Synthesize the big picture and analyze trends with BigQuery's AI.AGG function

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-29
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/deep-dive-into-bigquery-ai-agg-function/

## 核心主題
Google Cloud 介紹 BigQuery 新版 AI.AGG() 函數，讓開發者能在單一 SQL 查詢中以自然語言指令對百萬筆非結構化或多模態資料進行摘要與趨勢分析，無需將資料遷移至外部系統。

## 關鍵重點
- **非結構化資料的批次智能聚合**：AI.AGG() 採用多層聚合架構，自動將輸入資料切分批次處理後再整合結果，解決 LLM 上下文視窗限制。可應用於系統日誌分析（在無 FATAL 錯誤的情況下偵測記憶體、時鐘漂移等潛在問題）與產品目錄分類（自動識別類別並回傳 JSON 結構供後續 AI.CLASSIFY() 標記）。
- **多模態支援與 SQL 整合**：除了文字資料，AI.AGG() 原生支援影像輸入，可透過外部物件資料表直接將 GCS 圖片 URI 送入模型進行視覺內容總結。結果可與傳統 SQL 聚合、AI.CLASSIFY()、AI.IF() 等函數串聯，在同一查詢管道內完成從非結構化資料到結構化洞察的全流程。
- **最佳實踐與技術細節**：AI.AGG() 自動跳過 NULL 值，但 STRUCT 欄位若任一欄為 NULL 則整列被視為 NULL（可用 IFNULL() 補救）。總輸入 token 數可能因多層聚合而高於原始資料，建議使用 LIMIT 或預篩選降低 token 用量。可指定模型端點（如 gemini-2.5-flash），預設回傳字串格式，錯誤行會被排除但保留部分結果。

## 結論
AI.AGG() 將 BigQuery 的 AI 能力從「逐列分析」升級為「大規模聚合洞察」，讓企業能在既有資料倉儲中以單一 SQL 語法完成非結構化資料的趨勢總結、類別發現與異常偵測，大幅降低開發門檻並加速從原始資料到商業決策的價值鏈。
