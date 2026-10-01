# Empower your agents with the Google Cloud CLI remote MCP server

- **來源**: Google Cloud Blog AI & Machine Learning
- **發布日期**: 2026-10-01
- **原文連結**: https://cloud.google.com/blog/products/ai-machine-learning/google-cloud-cli-remote-mcp-server-in-preview/

## 核心主題
Google Cloud 推出 CLI remote MCP server，讓 AI 代理能安全地執行 gcloud 和 BigQuery 命令，無需本地安裝 CLI 工具。

## 關鍵重點
- **CLI 命令統一抽象**: 將數百個 gcloud 和 bq 命令打包成單一 MCP 伺服器，提供高階抽象，使 AI 代理能更直觀地執行複雜的雲端操作
- **雲端沙盒執行**: 無需本地安裝 CLI 工具，透過雲端沙盒執行，降低依賴管理和運行時維護的負擔
- **企業級安全機制**: 具備零環境憑證、Agent Identity 驗證、IAM 權限控制、Model Armor 保護以及完整的審計日誌功能
- **支援兩種命令工具**: 提供 run_gcloud_command 和 run_bq_command 兩種工具，讓 AI 代理能管理雲端基礎設施和 BigQuery 工作流
- **無額外費用**: 使用此 MCP 服務本身無額外費用，僅需為創建的 GCP 資源和數據傳輸成本付費

## 結論
Google Cloud CLI remote MCP server 為 AI 代理提供了管理 Google Cloud 基礎設施的新途徑，透過標準化的 MCP 協議實現安全、簡易的集成，同時保持企業級的安全標準。這將使 AI 代理能更輕鬆地執行雲端操作，無需擔心本地環境的複雜性。