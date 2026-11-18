# How to Build Durable Agentic Systems with Google Antigravity - From Instructions to Loops

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-18
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/how-to-build-durable-agentic-systems-with-google-antigravity-from-instructions-to-loops/

## 核心主題
Google Antigravity 平台如何建立可持續的代理系統，從單次指令轉向循環自動化。

## 關鍵重點
- **五個工作層級**：從簡單問題到系統，需要不同的自動化策略，系統層級需建立 AGENTS.md、skills、驗證閘門和監控儀表板
- **為什麼需要循環**：軟體開發基準從手動勞動轉向委託與編排，注意力是新瓶頸，循環可將成功率從 36% 提升至 95%
- **四大支柱**：可持續狀態（Git-backed checkpoints）、驗證閘門（測試必須在實現前撰寫）、評估（對無法確定驗證但重要的事項）、停止條件（轉數限制 20 步最佳和代幣/成本上限）
- **平台建議**：使用 `/goal` 命令執行自動化循環、`/grill-me` 進行互動式訪談、建立標準化技能（SKILL.md）和專案不變性（AGENTS.md）、採用跨模型審查機制
- **雙子代理架構**：researcher 負責搜尋程式碼庫並總結實現路徑，feature_implementer 負責實作程式碼變更並保持測試通過
- **預算限制機制**：設定 max_model_calls=20 次呼叫限制，以及 max_total_tokens=200,000 的總代碼限制，超出時會停止執行
- **驗證閘門與重試策略**：執行後會驗證輸出結果，若驗證失敗則觸發一次修正嘗試，若仍失敗則返回 False 交由人工處理，每個階段最多重試一次

## 結論
Google Antigravity 平台提供了一套完整的循環自動化框架，通過雙子代理架構、預算限制和驗證機制，幫助開發者建立可持續的代理系統。人類監督仍是必要的，以確保自動化輸出品質。

---