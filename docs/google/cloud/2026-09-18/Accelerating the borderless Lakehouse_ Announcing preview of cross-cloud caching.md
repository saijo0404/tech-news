# Accelerating the borderless Lakehouse: Announcing preview of cross-cloud caching

- **來源**: Google Cloud Blog Data Analytics
- **發布日期**: 2026-09-19
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/borderless-lakehouse-cross-cloud-caching-and-connections/

## 核心主題
Google Cloud 推出跨雲快取與連線功能，加速跨雲資料查詢並降低資料傳輸成本。

## 關鍵重點
- **跨雲快取功能**：透過快取頻繁存取資料，將跨雲資料傳輸量降低至 5% 以下，使跨雲分析與 AI 在企業規模下更具成本效益。
- **BigQuery 跨雲連線**：支援查詢非 Iceberg 格式資料（如 CSV、JSON、Parquet），提供完整 BigQuery 功能對等性，包括 AI 與 Gemini 功能。
- **細粒度快取機制**：採用子檔案區塊粒度，僅傳輸查詢所需的資料區塊，避免傳輸整個多吉比資料檔案。
- **企業級安全與合規**：快取資料預設使用 Google 管理加密鍵（GMEK）加密，並嚴格遵循多租戶隔離與區域資料駐留要求。

## 結論
透過結合 Iceberg 欄位式壓縮與跨雲快取，Google Cloud 大幅降低跨雲資料查詢的總擁有成本（TCO），使企業能更經濟地進行跨雲分析與 AI 工作負載。

---