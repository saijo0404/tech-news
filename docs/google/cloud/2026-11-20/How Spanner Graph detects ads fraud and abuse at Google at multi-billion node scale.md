# How Spanner Graph detects Google Ads fraud and abuse

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-21
- **原文連結**: https://cloud.google.com/blog/products/databases/how-spanner-graph-detects-google-ads-fraud-and-abuse/

## 核心主題
Google 使用 Spanner Graph 建立圖基平台，在數百億節點規模下即時偵測廣告詐騙與濫用行為，透過多跳關係分析識別惡意資產網絡。

## 關鍵重點
- **全球詐騙成本高昂**：2025 年全球詐騙損失近 5800 億美元，Google 2025 年已阻擋超過 83 億則違規廣告並暫停 2490 萬個廣告主帳號。
- **傳統方法失效**：詐騙行為形成網絡結構，單一指標分析無法捕捉關聯風險，且離線 MapReduce 批處理導致數小時延遲。
- **Spanner Graph 解決方案**：利用現有 Spanner 關係表直接疊加圖結構，實現秒級多跳查詢，無需數據遷移即可在數週內完成轉型。
- **5000 億節點實時圖**：平台現已管理超過 5000 億節點與 1 兆條邊，透過 ISO GQL 原生圖查詢語言進行即時模式匹配。
- **跨產業應用價值**：廣告、零售、資安、金融等領域均可利用此架構解決複雜模式匹配與詐騙挑戰。

## 結論
Spanner Graph 成功將 Google 的廣告詐騙偵測平台從小時級批處理升級為秒級實時偵測，不僅保護廣告主預算與用戶安全，更為其他企業提供可複製的實時圖智能解決方案。