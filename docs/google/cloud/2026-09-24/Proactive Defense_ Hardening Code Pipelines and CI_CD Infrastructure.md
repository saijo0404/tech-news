# Hardening Code Pipelines and CI_CD Infrastructure

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-24
- **原文連結**: https://cloud.google.com/blog/topics/threat-intelligence/hardening-code-pipelines-and-ci-cd-infrastructure/

## 核心主題
文章探討如何強化 CI/CD 管道與基礎設施以應對安全威脅，透過全週期自動化驗證建立韌性架構，將攻擊面最小化。

## 關鍵重點
- **端點安全與開發者工作站標準化**：統一安全層、本地秘密掃描、IDE 標準化與第三方外掛程式審查
- **程式碼儲存庫管理**：公司管理用戶模型、分支保護政策、禁止直接合併至主分支
- **憑證生命週期自動化**：自動化金鑰輪換、SSH 認證取代 PAT、GitHub Apps 取代服務帳號
- **依賴安全與 SBOM 生成**：禁止動態版本範圍、強制 SemVer 鎖定、建置階段生成簽名 SBOM
- **CI/CD 管道強化措施**：依賴冷卻期（7 天）、中央代理隔離、容器簽名與不可變摘要引用
- **最小權限原則**：OIDC 短期憑證、預設零權限 Runner、禁止憑證自動繼承
- **多層掃描閘門**：秘密掃描、SAST、SCA、容器掃描、DAST、CSPM 全週期驗證
- **活躍基礎設施保護**：WAF、API 閘道、微分段、配置完整性驗證與持續監控

## 結論
傳統點在時安全掃描已不足，需實施全週期自動化驗證，統一安全態勢，確保入侵快速隔離。
---
