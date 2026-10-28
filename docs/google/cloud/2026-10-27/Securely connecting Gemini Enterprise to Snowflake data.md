# Securely connecting Gemini Enterprise to Snowflake data

- **來源**: Google Cloud Blog Data Analytics
- **發布日期**: 2026-10-28
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/bridge-gemini-enterprise-and-snowflake-with-google-adk/

## 核心主題
這篇文章介紹如何使用 Google ADK 和 Model Context Protocol (MCP) 安全地將 Gemini Enterprise 與 Snowflake 數據庫連接，讓 AI 代理能夠生成 SQL 並執行查詢，同時保持嚴格的安全性和數據治理。

## 關鍵重點
- **OAuth 身份驗證**：使用 OAuth 2.0 進行用戶身份驗證，避免使用通用服務帳戶，確保最小權限原則，防止安全風險
- **治理翻譯**：ADK 代理將用戶的自然語言問題傳遞給 Snowflake MCP 伺服器，由 Cortex 代理（CORTEX_AGENT_RUN）進行翻譯並執行
- **治理邊界**：查詢執行完全限制在 Snowflake 的治理邊界內，減少 schema 幻覺和未驗證 SQL 執行的風險
- **專用角色**：在 Snowflake 內創建專用角色，僅授予必要權限，並設置 DEFAULT_ROLE 和 DEFAULT_WAREHOUSE
- **Python 實現**：使用 Google ADK 和 gemini-2.5-flash 模型構建代理，通過 McpToolset 連接 Snowflake MCP 伺服器

## 結論
此架構為企業 AI 提供了安全、治理的數據訪問方式，同時保持用戶級權限和最小權限原則，適合複雜的多代理系統開發。

---