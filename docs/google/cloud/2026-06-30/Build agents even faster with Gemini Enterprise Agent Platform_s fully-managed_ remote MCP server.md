# Build agents even faster with Gemini Enterprise Agent Platform's fully-managed, remote MCP server

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-30
- **原文連結**: https://cloud.google.com/blog/products/ai-machine-learning/gemini-enterprise-agent-platform-remote-mcp-server/

## 核心主題
Google Cloud 推出 Gemini Enterprise Agent Platform 的**遠端 MCP Server**，讓開發者能從外部開發工具（如 Claude Code、Antigravity CLI）直接安全連線至 Google Cloud 資源，在 IDE 內即可完成模型呼叫、提示詞模板管理與 Notebooks 操作，無需離開開發環境。

## 關鍵重點
- **打通外部 IDE 與 Google Cloud 的橋樑**：Agent Platform MCP Server 作為橋接器，讓在外部 IDE 建構的 AI 代理能安全互動於 Agent Platform 資源——包括呼叫 Model Garden 的模型、拉取共享提示詞模板、以及在專案內直接管理 Notebooks。開發者不必在外部工具與雲端基礎設施之間來回切換。
- **開發速度與資安治理兼得**：MCP Server 提供單一標準化介面，減少整合程式碼的開發時間。內建於 Google Cloud 基礎設施中，預設由 Cloud IAM Deny 政策保護，IT 團隊可嚴格管控外部開發框架僅能存取授權資源，同時維持對開放 MCP 規格（Model Context Protocol）的相容性。
- **九大全功能 Toolset 端點**：涵蓋產生式 AI（generate）、預測（predict）、Colab Enterprise Notebooks（notebook）、端點管理（endpoints）、模型註冊（models）、模型微調（tuning）、品質評估（evaluation）、提示詞管理（prompts）等九大工具集，開發者可透過複製貼上方式直接使用。啟用步驟僅三步：開啟 API → 設定客戶端 → 使用工具集。

## 結論
透過遠端 MCP Server，Google Cloud 解決了「開發速度」與「IT 治理」之間的經典兩難——開發者能以最小設定在熟悉的 IDE 中加速建構 AI 代理，而企業仍可透過 IAM 政策和 Agent Registry 集中管理所有 AI 資產。這讓基於 MCP 標準的企業級 AI 代理開發變得更加直接且安全。

---
