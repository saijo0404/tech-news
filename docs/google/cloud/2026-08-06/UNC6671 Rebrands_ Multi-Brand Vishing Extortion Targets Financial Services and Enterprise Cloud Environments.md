# UNC6671 Rebrands: Multi-Brand Vishing Extortion Targets Financial Services and Enterprise Cloud Environments

- **來源**: Google Cloud Blog
- **發布日期**: 2026-08-06
- **原文連結**: https://cloud.google.com/blog/topics/threat-intelligence/unc6671-targets-financial-services-and-enterprise-cloud-environments/

## 核心主題
UNC6671 勒索軟體集團已重新品牌化，轉型為多品牌操作（包括 Redact、Pink、Helix 及 Falcon），專注於金融服務、私募股權及專業服務領域，透過語音詐騙（Vishing）和身份認證洩漏進行攻擊。

## 關鍵重點
- **攻擊手法**：主要透過語音詐騙（Vishing）偽裝為 IT 支援人員，使用 AiTM 基礎設施截獲 MFA 令牌，竊取 Microsoft 365 及 Okta 等雲端環境數據
- **目標產業**：近期轉向金融服務、私募股權及專業服務等領域，專注於涉及合併、收購及訴訟的高價值企業
- **防護措施**：強制實施抗釣魚多因素認證（FIDO2 憑證）、整合 SaaS 應用與統一身份認證、強化會話控制與權限管理
- **指標 (IOCs)**：提供 100+ 個 phishing 域名範例（如 myoktasso.com、mypasskeys.com）及多個 IP 地址（Private Layer 面板代理、MEVSPACE 後端等）
- **安全建議**：強制企業管理設備認證、端點與瀏覽器憑證保護、監控 IDP 日誌與 UAL 遥測、限制住宅代理認證

## 結論
此報告提供具體的防護指引和指標，幫助組織識別和阻斷身份中心型攻擊。特別感謝 researcher ZachXBT 協助加密貨幣分析。建議優先部署抗 phishing 驗證器與行為式 SaaS 審計，以阻斷身份中心型攻擊。

---