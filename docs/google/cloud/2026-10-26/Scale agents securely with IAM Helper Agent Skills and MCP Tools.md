# Scale agents securely with IAM Helper Agent Skills and MCP Tools

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-27
- **原文連結**: https://cloud.google.com/blog/products/identity-security/scale-agents-securely-with-iam-helper-agent-skills-and-mcp-tools/

## 核心主題
Google Cloud 推出 IAM Helper Agent Skills，幫助自主代理在 Google Cloud 上安全地管理身份和訪問控制，解決代理時代身份驗證與權限管理的挑戰。

## 關鍵重點
- **IAM Helper Agent Skills**：一套智能、代理面向的構件，可自動化複雜的端到端 IAM 工作流程，整合 Google Cloud 的核心 IAM 引擎（包括 Policy Intelligence 和 Privileged Access Manager PAM）。
- **基於 MCP 工具**：所有技能都基於 Google Cloud IAM MCP 工具，提供原子化、只讀函數，最大化 token 效率，讓代理能動態發現並調用這些工具執行基本操作。
- **內建防護措施**：將只讀診斷與政策變更分開，政策變更需要人類介入確認（HITL），根據可自訂的風險等級暫停。
- **四大核心功能**：
  - **iam-helper-for-policy-management**：生成和驗證 IAM v1 允許綁定和 v2 拒絕規則，自動阻止風險配置（如 public access 和 broad basic roles）。
  - **iam-helper-for-troubleshooting**：快速識別 403 錯誤的缺失權限或阻擋規則，根據用戶角色提供請求者或解決者流程。
  - **iam-helper-for-policy-simulator**：在實施變更前模擬影響範圍，測試提案變更與 90 天歷史訪問記錄，確保現有工作負載不會中斷。
  - **iam-helper-for-privileged-access-management**：管理即時訪問的生命週期，支持請求者、管理員和批准者工作流程，確保訪問經過審計、時間限制，並在任務完成後自動撤銷。
- **跨代理兼容**：可在 Gemini CLI、Gemini Cloud Assist、ADK、Claude Code 和 Cursor 等常見代理上運行。

## 結論
IAM Helper Agent Skills 通過自動化複雜的 IAM 工作流程，大幅減少管理開銷，加速部署速度，同時確保最小權限原則和代理治理，是組織在採用自主代理時應對身份和訪問管理挑戰的關鍵解決方案。

---