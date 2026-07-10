# The _Ghost_ in the Database_ Recovering Active ADFS Signing Keys via Machine DPAPI

- **來源**: cloud.google.com/blog
- **發布日期**: 2026-07-08
- **原文連結**: https://cloud.google.com/blog/topics/threat-intelligence/recovering-active-adfs-signing-keys-machine-dpapi/

## 核心主題
這篇文章揭露了 ADFS 簽名密鑰可能透過 Machine DPAPI 被恢復的漏洞，允許攻擊者偽造 SAML 令牌並繞過身份驗證控制。

## 關鍵重點
- **漏洞成因**：當 AutoCertificateRollover 被禁用且手動旋轉證書時，WID 資料庫可能保留舊證書記錄，形成「鬼證書」，但實際簽名密鑰仍存於 Machine DPAPI 中
- **攻擊流程**：攻擊者透過 SYSTEM 級權限訪問 Machine DPAPI 儲存，恢復 ADFS 簽名私鑰，偽造 SAML 令牌，繞過多因素認證和條件訪問控制
- **防禦措施**：將 ADFS 視為 Tier 0 身份基礎設施，使用硬體安全模組保護密鑰、使用 gMSA 服務身份、實施嚴格的管理控制，並確保證書旋轉時同步更新資料庫

## 結論
ADFS 簽名密鑰的 Machine DPAPI 儲存機制雖然確保了服務韌性，但也引入了安全風險，組織需要實施多層防禦策略並定期驗證證書配置一致性，以防止身份偽造攻擊。

---
