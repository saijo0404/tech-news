# Expanding Managed Agents in Gemini API

- **來源**: Google Blog
- **發布日期**: 2026-07-07
- **原文連結**: https://blog.google/innovation-and-ai/technology/developers-tools/expanding-managed-agents-gemini-api/

## 核心主題
Google Gemini API 擴展了 Managed Agents 的功能，包括背景執行、遠端 MCP 伺服器整合、自訂函數呼叫和憑證刷新，使開發者能建立更可靠、可上線的自主代理。

## 關鍵重點
- **背景執行 (Background Execution)**：支持長時間運行的異步任務，立即返回 ID，客戶端可後續查詢狀態或重新連接
- **遠端 MCP 伺服器整合**：允許 managed agents 直接連接遠端 Model Context Protocol 伺服器，無需自訂代理中間件，可混合使用遠端工具與沙盒能力
- **自訂函數呼叫**：可在沙盒工具之外添加自訂工具，使用 step matching 機制，自訂函數會轉換為 requires_action 狀態
- **憑證刷新**：支持刷新存取金鑰和短期 API 金鑰，使用相同的 environment_id 和新的網路配置，沙盒狀態保持完整

## 結論
這些更新將 managed agents 轉變為可在真實開發環境中運行的異步工作員，無需阻塞應用程式，直接回應開發者反饋與產品需求。

---

檔案已成功儲存至指定路徑。