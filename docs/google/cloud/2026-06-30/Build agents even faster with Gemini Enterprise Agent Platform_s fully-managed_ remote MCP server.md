# Build agents even faster with Gemini Enterprise Agent Platform's fully-managed, remote MCP server

- **來源**: Google Cloud Blog AI & Machine Learning
- **發布日期**: 2026-07-01
- **原文連結**: https://cloud.google.com/blog/products/ai-machine-learning/gemini-enterprise-agent-platform-remote-mcp-server/

## 核心主題
這篇文章介紹了 Gemini Enterprise Agent Platform 提供的遠端 MCP 伺服器，讓外部 AI 代理能安全地連接到 Google Cloud 環境內的資源，加速 AI 代理的開發與部署。

## 關鍵重點
- **橋接開發工具與雲端架構**：Agent Platform MCP 伺服器作為外部開發工具（如 Antigravity CLI、Claude Code）與 Google Cloud 環境之間的橋樑，讓代理能安全地調用 Model Garden 模型、下載提示模板或管理 Notebooks。
- **提升時間效率與安全性**：提供單一標準化介面，減少整合代碼時間，同時在 Google Cloud 安全基礎設施內運行，保護數據並加速開發。
- **開源標準與集中化管理**：支援開源 MCP 規範，外部 IDE 可無縫互動；透過 Agent Registry 集中管理資產，IT 團隊可運用原生 Cloud IAM 策略確保外部開發框架僅與授權資源互動。
- **三步簡易連接**：啟用 API、配置客戶端、使用工具集，即可快速開始使用。提供多種工具集（如生成、預測、Notebook、端點管理等）供開發者直接使用。

## 結論
透過使用 Gemini Enterprise Agent Platform 的遠端 MCP 伺服器，開發者可以更安全、更快速地構建 AI 代理，同時保持對數據和資源的完整管控，實現開發效率與安全治理的最佳平衡。

---