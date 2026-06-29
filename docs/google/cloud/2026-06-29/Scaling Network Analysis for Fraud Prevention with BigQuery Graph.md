# Scaling Network Analysis for Fraud Prevention with BigQuery Graph

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-29
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/fraud-prevention-with-bigquery-graph/

## 核心主題
英國金融 super-app Curve 透過導入 BigQuery Graph 的原生圖分析能力，突破傳統關聯式資料庫在多跳（multi-hop）分析上的瓶頸，以高效方式揭開隱藏的詐騙網絡並大幅減少交易損失。

## 關鍵重點
- **多跳分析的運算挑戰**：詐騙集團常在多個帳戶間共用裝置、資金卡或聯絡資訊，傳統 SQL 需要大量自我關聯（self-joins）才能追蹤這些鏈結，在數百萬用戶與數千萬筆連接的規模下，查詢變得極度耗時且難以維護。
- **BigQuery Graph 原生圖分析優勢**：Curve 將支付生態系建模為屬性圖（節點為使用者、邊為共用的識別欄位），以 GQL 語法取代複雜的 JOIN 邏輯。資料保留在 BigQuery 內無需遷移，並可將圖遍歷與標準 SQL 分析、機器學習工作流結合於單一查詢中。
- **具體成效與未來規劃**：2025 年自動化阻擋機制節省約 1,200 萬美元交易損失，圖驅動的查詢在識別詐騙使用者上達到約 72% 精確度。GQL 讓 Curve 能更頻繁地更新詐騙規則並加速圖特徵供應給 ML 模型，目前正著手將數十億筆 IP 地址連接納入即時偵測循環。

## 結論
Curve 的案例證明，將資料視為關係網絡而非表格中的資料列，能顯著提升金融詐騙偵測的效率與準確性。BigQuery Graph 讓企業能在既有資料倉儲環境中實現大規模圖分析，無需額外遷移或學習新語言，為反詐騙防禦提供了兼具成本效益與擴展性的解決方案。
