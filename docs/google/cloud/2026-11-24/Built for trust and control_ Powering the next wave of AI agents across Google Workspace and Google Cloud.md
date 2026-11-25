# Built for trust and control: Powering the next wave of AI agents across Google Workspace and Google Cloud

- **來源**: Google Cloud Blog Security & Identity
- **發布日期**: 2026-11-25
- **原文連結**: https://cloud.google.com/blog/products/identity-security/deploying-agents-safely-in-your-enterprise/

## 核心主題
Google Workspace 與 Google Cloud 推出新一代 AI 代理介面，在提供開發者現代化工具的同時，強化企業級安全控制與信任機制。

## 關鍵重點
- **專用介面推出**：Workspace MCP 伺服器、Workspace CLI 與 Cloud Agent Gateway 全面推出，提供標準化、安全且符合代理原生協議的介面。
- **統一安全模型**：所有代理請求都經過政策檢查、權限驗證、DLP 規則篩選與提示入侵防護（Model Armor）。
- **明確的權限與確認機制**：代理必須使用獨立 OAuth 客戶 ID，關鍵操作需人類確認，並有使用限制與計費機制。
- **可視化與撤銷能力**：管理員可監聽代理活動並即時撤銷存取權限，用戶也能檢視並撤銷代理存取。
- **嚴格資料邊界**：禁止代理進行永久儲存、模型訓練或資料爬蟲，敏感資料透過加密與存取控制加以保護。

## 結論
Google 透過 Workspace MCP 與 CLI 的推出，讓開發者能建立可靠且安全的 AI 代理，同時讓企業擁有完整的可視化與控制能力，在加速 AI 採用的同時降低風險。

---