# Gemini API Managed Agents: 3.6 Flash, hooks, and more

- **來源**: Google Blog
- **發布日期**: 2026-07-28
- **原文連結**: https://blog.google/innovation-and-ai/technology/developers-tools/expanding-managed-agents-gemini-api-3-6-flash-hooks/

## 核心主題
Google Gemini API 的 Managed Agents 服務推出重大更新，預設模型升級為 Gemini 3.6 Flash，並新增環境 hooks、預算控制、定時觸發與免費等級存取等關鍵功能。

## 關鍵重點
- **預設模型升級**：antigravity-preview-05-2026 代理預設使用 Gemini 3.6 Flash，無需程式碼修改即可自動採用新模型。
- **環境 hooks 功能**：新增環境 hooks 允許開發者在沙盒中阻擋、檢查或審計代理的工具呼叫，支援 regex 匹配與多階段處理。
- **成本與預算控制**：Managed Agents 現已開放免費等級存取，並新增 max_total_tokens 預算限制，防止任務無限制消耗。
- **定時觸發機制**：支援透過 cron 定時自動執行代理任務，環境狀態會保留以便後續繼續執行。
- **實際應用案例**：投資銀行 OffDeal 利用 hooks 在沙盒中執行圖像驗證，確保合規性與品質標準。

## 結論
這些更新將 Managed Agents 轉化為更具成本效益、可定時自動化且具備嚴格控制能力的生產級工具，使開發者能更安全、可控地部署 AI 代理到真實開發環境中。
---
