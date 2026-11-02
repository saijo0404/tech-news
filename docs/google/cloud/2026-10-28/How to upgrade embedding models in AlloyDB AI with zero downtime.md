# How to upgrade embedding models in AlloyDB AI with zero downtime

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-28
- **原文連結**: https://cloud.google.com/blog/products/databases/upgrade-embedding-models-in-alloydb-ai-with-zero-downtime/

## 核心主題
這篇文章介紹如何在 PostgreSQL AlloyDB AI 中實現嵌入模型的零停機升級，透過自動嵌入、ScaNN 索引和原子切換策略，讓用戶無需計劃停機即可升級模型。

## 關鍵重點
- **動態模型切換**：透過 GUC 變數 `app.embedding_model` 與表值函數實現模型動態切換，支援 Canary A/B 測試，可輕鬆回滾
- **自動嵌入功能**：背景快速生成新嵌入（每秒最高 3000 條），支援交易型（即時一致）或手動模式，保持數據即時更新
- **ScaNN 索引優勢**：索引建立速度快 10 倍（10 萬行 3072 維模型約 50 秒 vs HNSW 7-13 分鐘），支援並行索引創建
- **兩種切換策略**：模式 A（原子列重命名）支援零代碼變更；模式 B（GUC+SRF）支援 Canary 測試與交易型自動嵌入
- **資源規劃**：新模型（gemini-embedding-001）儲存空間約為舊模型（text-embedding-005）的 3 倍，1000 萬行資料需約 133 GB 新向量欄位空間
- **交易模式升級**：若使用 transactional 模式，可跳過自動刷新步驟，但寫入延遲會增加（從 37.5ms 升至 191ms）

## 結論
AlloyDB AI 結合 PostgreSQL 原生功能與 AI 能力，提供零停機升級方案，讓 DBA 與開發者能即時更新嵌入模型，同時保持數據一致性和性能。透過標準化查詢、連接池注意事項及批次退役舊模型等最佳實踐，確保升級過程安全且高效。

---