# Unifying enterprise context and semantics: LookML in Knowledge Catalog is now GA

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-27
- **原文連結**: https://cloud.google.com/blog/products/business-intelligence/lookml-metadata-indexing-in-knowledge-catalog-is-now-ga/

## 核心主題
Google Cloud 正式推出 LookML 語義語言索引功能，將 LookML 的確定性業務邏輯自動索引到 Knowledge Catalog，使 AI 代理能同時獲得企業級上下文和精確的 BI 語義定義。

## 關鍵重點
- **雙層架構整合**：Knowledge Catalog 提供企業級上下文（資料資產、治理、資料鏈結），而 LookML 提供確定性的數學語義（指標計算、關聯邏輯、過濾規則），兩者結合解決 AI 代理在直接查詢原始資料庫時的指標定義漂移和盲目關聯擴展問題。
- **多層級實體索引**：支援 LookML 模型、Explores、Views、欄位、儀表板等多層級實體的自動索引，包含完整的關聯邏輯、過濾規則和資料驗證測試。
- **即時同步機制**：資料同步預設開啟，任何生產環境的 LookML 更新會在近實時時間內反映到 Knowledge Catalog，確保 AI 代理始終使用最新的業務邏輯。
- **Gemini Enterprise 整合**：Gemini Enterprise 可透過此整合自動發現 LookML 語義並生成準確的 SQL，無需額外程式碼，並支援透過 LookupContext API 供自訂代理使用。

## 結論
透過將 LookML 業務邏輯整合到 Knowledge Catalog，企業可建立更準確、可治理且高效能的 AI 代理工作流。此功能使 Looker Conversational Analytics（專注 BI 內部）與 Knowledge Catalog + Looker（企業級 AI 助手）形成互补，讓使用者在 Looker 內部進行自服務資料探索，同時在 Gemini Enterprise 中跨多個資料來源獲得精確的業務分析。

---