---
# Securing agentic AI with perimeter guardrails: What's new in VPC Service Controls

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-26
- **原文連結**: https://cloud.google.com/blog/products/identity-security/securing-agentic-ai-whats-new-in-vpc-service-controls/

## 核心主題
Google Cloud 宣布 VPC Service Controls（VPC-SC）推出針對 Agentic AI 工作負載的新功能，包括代理身份支援、MCP 屬性細粒度控制，以及 Gemini Enterprise Agent Platform 的原生整合，為自主 AI 智能體提供網路層級的資料安全防護網。

## 關鍵重點
- **代理身份與 MCP 屬性細粒度控制**：VPC-SC 現支援將 AI 智能體視為一等公民身份（agentic identities），直接加入服務邊界的出入站規則，使用標準 IAM 主體或 principalSet 管理智能體群組的存取權限，一旦智能體遭入侵可立即撤銷。同時支援基於模型上下文協議（MCP）屬件的條件存取規則，可根據 `mcp.toolName`、`mcp.method` 與 `mcp.tool.isReadOnly` 等屬性限制智能體的工具使用（如允許讀取但不允許發送郵件）。
- **Gemini Enterprise Agent Platform 原生安全整合**：VPC-SC 現已原生整合 Gemini Enterprise Agent Platform。當將 Agent Platform 加入受保護服務範圍後，系統會自動阻擋所有對該平台的公開網際網路存取，無需額外的組態設定即可強制執行安全邊界。
- **抵禦 OWASP Agentic AI 特有攻擊向量**：VPC-SC 作為目的地為基礎的防禦，可有效阻擋三大攻擊途徑：（1）間接提示注入（OWASP ASI01）導致的資料外洩——即使智能體擁有有效 IAM 權限，VPC-SC 仍會阻擋資料傳送至邊界外的 webhook；（2）工具濫用（OWASP ASI02、ASI08）——防止惡意提示鏈接工具將內部資料橋接至隔離信任區外；（3）內部威脅（OWASP ASI03）——阻擋攻擊者命令資料處理智能體將 BigQuery 資料直接複製至未授權專案，即使網路防火牆與 IAM 均視為合法流量，VPC-SC 仍會根據目的資源拒絕請求。

## 結論
在自主 AI 智能體的時代，邊界安全已從最佳實踐升級為絕對必要條件。VPC Service Controls 提供 IAM 無法單獨實現的資料流動控制——在智能體將提示視為程式碼的時代，VPC-SC 成為企業資料的強制性安全網。結合 IAM 的映射能力與 VPC-SC 剛性的資料邊界，組織能在確保資料不外洩的前提下，安心推動 Agentic AI 創新。

---
