# Agentic Resource Discovery: Let agents search for tools, skills, and other agents

- **來源**: HuggingFace Blog
- **發布日期**: 2026-06-17
- **原文連結**: https://huggingface.co/blog/agentic/resource-discovery-launch

## 核心主題
Agentic Resource Discovery（ARD）是一套由 Microsoft、Google、Hugging Face 等公司共同開發的開放規格，旨在解決 AI Agent 在執行階段動態發現與搜尋工具、技能及其他 Agent 的問題，將能力選取從 LLM 上下文外移至結構化搜尋層。

## 關鍵重點
- **解決「先安裝後使用」的擴展瓶頸**：當前 Agent 能力管理依賴硬編碼設定或將所有工具描述塞入上下文視窗，兩者皆無法擴展至數千種工具。ARD 透過靜態 manifest（ai-catalog.json）與動態搜尋 API（POST /search）建立聯合登記系統，讓 Agent 能根據自然語言意圖在執行階段動態發現所需能力，無需預先安裝。
- **Hugging Face Discover 工具實作**：Hugging Face 推出 hf-discover 作為 ARD 的參考實作，整合 Hub 的 Semantic Search 提供數千個 Skills、ML 應用與 MCP Servers 的搜尋存取。支援三種媒體類型：application/ai-skill（預設，自動將 Space 的 agents.md 包裝為技能）、application/mcp-server+json（MCP 伺服器目錄），以及 application/vnd.huggingface.space+json（原始 Space 元數據）。
- **多管道存取與聯合架構**：提供 Hugging Face CLI（hf discover search）、REST API（POST https://huggingface-hf-discover.hf.space/search）與 MCP 端點三種存取方式。規格設計為去中心化聯合架構，任何公司可獨立實作，搜尋單一服務即可發現其他服務託管的能力，未來將進一步支援 auto、referrals、none 三種聯合模式。

## 結論
ARD 將 Agent 能力管理從靜態配置轉化為意圖驅動的動態搜尋生態系，Hugging Face 的 Discover 工具已提供可直接使用的實作，為 MCP、A2A 與 Skills 協議提供了缺失的「發現層」，讓 Agent 能自主探索並整合不斷擴展的工具與服務網絡。

---
