# Introducing TimesFM 3.0 with multivariate time-series forecasting in BigQuery

- **來源**: Google Cloud Blog Data Analytics
- **發布日期**: 2026-10-13
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/bigquery-timesfm-3-0-with-multivariate-time-series-forecasting/

## 核心主題
BigQuery 正式推出 TimesFM 3.0，首次支援多變量時間序列預測，讓企業可在熟悉的 SQL 工作流中直接進行高階時間序列分析，無需訓練或管理自訂模型。

## 關鍵重點
- **多變量預測能力**：TimesFM 3.0 支援同時預測多個相關目標（如通勤與休閒騎乘量），並能捕捉跨系列動態關係
- **完整協變量支援**：可整合過去、現在和未來的協變量（如天氣、週末指標、促銷活動），提升預測準確度
- **企業級精度**：在 GIFT-Eval、FEV-Bench 和 TIME 三大公開排行榜上均排名第一，零樣本預測準確度領先現有基礎模型
- **即插即用升級**：與 AI.FORECAST 和 AI.DETECT_ANOMALIES 完美整合，只需指定 model => 'TimesFM 3.0' 即可立即提升現有工作流精度
- **自然語言分析**：支援 BigQuery 對話式分析，透過自然語言指令即可生成多變量預測與互動式預測圖表

## 結論
TimesFM 3.0 標誌著 BigQuery 時間序列分析能力的重大突破，讓企業無需複雜的數據移動、特徵工程或專屬模型託管基礎設施，即可在 SQL 中直接進行企業級多變量預測分析。

---