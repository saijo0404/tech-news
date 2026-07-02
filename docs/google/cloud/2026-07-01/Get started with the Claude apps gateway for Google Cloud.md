---
# Get started with the Claude apps gateway for Google Cloud

- **來源**: Google Cloud Blog
- **發布日期**: 2026-07-01
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/announcing-claude-apps-gateway-for-google-cloud/

## 核心主題
Anthropic 推出 **Claude apps gateway**——一套自託管閘道服務，部署於 Google Cloud Run 上，作為開發者本地 Claude Code 客戶端與 Google Cloud Agent Platform 之間的中介層，讓企業能集中治理身份、政策、成本與流量路由。

## 關鍵重點
- **解決企業級 AI 編碼工具部署摩擦**：個別開發者只需設定 `CLAUDE_CODE_USE_VERTEX=1` 即可將 Claude Code 指向 GCP 專案，但組織級部署面臨多重痛點——管理每人的雲端憑證、透過 MDM 推送設定檔、缺乏逐人用量歸因與支出上限。Claude apps gateway 解決這些問題：①**身份集中治理**——登入請求經 IdP（Google Workspace 或任何 OIDC）驗證，閘道交換為短期 Session Token，開發者筆電上不存放任何敏感憑證；入職加入 IdP 群組、離職移除群組即生效。②**政策伺服器端強制**——RBAC 規則寫在 `gateway.yaml` 中，每呼叫一次即重新檢查 `availableModels`，編輯本地 `managed-settings.json` 無法繞過。③**可驗證的遙測**——所有 `claude_code.token.usage` 指標攜帶經過驗證的 Email 與群組資訊，透過 OTLP/HTTP 送至企業監控系統。④**支出上限控制**——透過管理 API 設定每日、每週或每月用量上限，閘道以 Cloud SQL 記錄並超量回傳 429。
- **架構與部署步驟**：Gateway 是部署於 **Cloud Run** 的無狀態容器，開發者的 Claude 程序透過 HTTPS 送推論流量至閘道。閘道驗證 Session Bearer Token、檢查政策後，使用 Cloud Run 服務帳號轉發至 Agent Platform。**Cloud SQL Postgres** 存放登入狀態與支出帳本，**OTLP 收集器**接收歸因指標。四步部署流程：①啟用 Agent Platform、Cloud SQL、Secret Manager API，建立服務帳號。②撰寫 `gateway.yaml` 指向 OIDC 客戶端、Postgres 連線字串與 Agent Platform 上游。③部署至 Cloud Run（支援 GKE 替代方案）。④透過 MDM 推送 `managed-settings.json` 強制登入閘道 URL。
- **流量路由與未來擴充**：所有請求使用單一 Cloud Run 服務帳號身份發出，可設定 `region: global` 使用 Agent Platform 全域端點，或增加第二個 `upstreams` 項目實現 5xx/429/timeout 時的故障轉移。推論全程保留在 GCP 專案內，配额、資料處理協議與計費均不變。未來規劃包括群組範圍政策（按群組分配不同模型清單與工具權限）。

## 結論
Claude apps gateway 的本質是一個**企業級 AI 編碼工具的管理中樞**——將分散在開發者筆電上的 Claude Code 連線集中到閘道後，企業就能以與管理傳統企業軟體相同的方式治理 AI 編碼工具：控制誰能用、能用什麼模型、花多少錢、以及所有使用行為的可追蹤性。這讓 Anthropic 的 AI 編碼工具從「個人開發者玩具」升級為「企業正式部署方案」。

---
