# SOCRadar powers rapid threat detection with AlloyDB and Gemini Enterprise

- **來源**: Google Cloud Blog
- **發布日期**: 2026-07-01
- **原文連結**: https://cloud.google.com/blog/products/databases/socradar-powers-rapid-threat-detection-with-alloydb-and-gemini-enterprise/

## 核心主題
網路安全公司 SOCRadar 從自建 PostgreSQL 遷移至 Google Cloud **AlloyDB**，獲得 **20 倍效能提升**、釋放 **75% DBA 人力**並回收 **45 TB 儲存空間，再結合 **Gemini Enterprise Agent Platform** 以 AI 過濾安全警報，徹底解決安全營運中心（SOC）長期以來面臨的「警報疲勞」問題。

## 關鍵重點
- **"三合一"負載處理與 3.2 倍資料 ingestion 提升**：SOCRadar 每日處理來自數千個異質來源（暗網論壇、botnet 日誌、社群媒體）的即時威脅資料，AlloyDB 成功應對其「三威脅」查詢環境：①**高頻率交易式資料擷取**（OLTP）：即時 INSERT/UPSERT 操作速度提升 **3.2 倍**，確保最新威脅指標立即可用。②**即時操作型查詢**：在零負載條件下，原本需 3-3.5 秒的索引查詢降至 **1 秒**。③**深度分析聚合**（OLAP）：利用內建記憶體列式引擎，分析查詢速度提升高達 **20 倍**。
- **節省 75% DBA 時間與 45 TB 儲存回收**：AlloyDB 的智慧記憶體管理與寫入前日誌（WAL）最佳化消除了持續手動調校的need，DBA 系統檢查頻率降至每 2-3 天一次。其動態儲存管理更在清除歷史日誌後**立即回收 45 TB 儲存空間**——傳統資料庫需為已刪除的固定預配儲存空間付費，而 AlloyDB 會自動縮小至實際使用量。
- **Gemini Enterprise 整合與未來 Agentic AI 藍圖**：SOCRadar 將 Gemini Enterprise Agent Platform 直接整合至 AlloyDB 上的警報管理框架，AI 原生過濾可自動區分真正威脅與誤報，在警報送達使用者前即完成分類、過濾與路由。未來計畫推出三大功能：**自然語言查詢**（讓分析師以對話式語言進行威脅搜尋）、**語意相似性搜尋**（利用原生向量嵌入發現傳統關鍵字搜尋遺漏的隱藏模式）、**自動化事件摘要**（將複雜技術日誌即時轉為簡明白話摘要）。

## 結論
SOCRadar 的案例展示了「效能基礎設施 + AI 能力」如何共同重塑網路安全營運——AlloyDB 消除了資料瓶頸，讓交易速度與歷史分析在同一平台上並行不悖；Gemini Enterprise 則將海量警報轉化為可行動的洞察。兩者的結合不僅解決了當下問題，更為自主式 AI 威脅獵捕奠定了堅實基礎。

---
