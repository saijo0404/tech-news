# Expanding Managed Agents in Gemini API_ background tasks_ remote MCP and more

- **來源**: blog.google/innovation-and-ai/technology/developers-tools/expanding-managed-agents-gemini-api/
- **發布日期**: 2026-07-07
- **原文連結**: https://blog.google/innovation-and-ai/technology/developers-tools/expanding-managed-agents-gemini-api/

## 核心主題
Google 擴展 Gemini API 的 Managed Agents 功能，新增背景執行、遠端 MCP 伺服器整合、自訂函數呼叫和憑證刷新等能力，讓開發者能建立更可靠、生產級別的代理系統。

## 關鍵重點
- **背景執行**：允許長程任務在伺服器上異步執行，不阻塞應用程式，API 立即返回 ID 供客戶端追蹤進度
- **遠端 MCP 伺服器整合**：讓代理直接連接遠端 Model Context Protocol 伺服器，無需自訂代理中間件，可混合使用遠端工具與內建沙盒能力
- **自訂函數呼叫**：允許在沙盒工具之外添加自訂工具，API 使用步驟匹配，自訂函數可轉換為需要客戶端執行本地業務邏輯
- **憑證刷新**：允許在下次互動時刷新網路憑證或旋轉金鑰，不丟失沙盒檔案系統狀態、已安裝套件和克隆倉庫

## 結論
透過這些更新，Managed Agents 轉變為異步工作員，能在真實開發環境中運作而不阻塞應用程式，讓開發者能建立更可靠、可擴展的代理系統。

---
