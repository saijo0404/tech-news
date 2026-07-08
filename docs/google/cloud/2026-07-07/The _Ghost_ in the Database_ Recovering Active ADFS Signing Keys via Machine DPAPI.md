# The 'Ghost' in the Database: Recovering Active ADFS Signing Keys via Machine DPAPI

- **來源**: Google Cloud Blog Threat Intelligence
- **發布日期**: 2026-07-08
- **原文連結**: https://cloud.google.com/blog/topics/threat-intelligence/recovering-active-adfs-signing-keys-machine-dpapi/

## 核心主題
這篇文章揭露了攻擊者如何利用 ADFS 證書配置漂移（ghost certificate）透過 Machine DPAPI 提取有效的簽名私鍵，進而偽造高權限 SAML 令牌，繞過多因素認證和身份控制。

## 關鍵重點
- 當 ADFS 證書手動旋轉且 AutoCertificateRollover 功能關閉時，WID 資料庫會保留過期的證書記錄，形成「鬼影」證書，導致攻擊者仍能提取到有效私鍵
- 攻擊者透過 SYSTEM 權限存取 Machine DPAPI 儲存（C:\ProgramData\Microsoft\Crypto\RSA\MachineKeys\ 和 C:\Windows\System32\Microsoft\Protect\S-1-5-18\），可提取到 ADFS 服務的有效簽名私鍵，無需接觸 LSASS 或 ADFS 服務進程
- 此攻擊向量可偽造 Global Administrator 權限的 SAML 令牌，繞過 MFA 和條件存取控制，使攻擊者能無權限訪問 Microsoft 365 和 Entra ID

## 結論
組織應將 ADFS 視為 Tier 0 身份基礎設施，採用 HSM 保護私鍵、啟用 AutoCertificateRollover、監控 Event ID 385 並驗證證書一致性，以減少配置漂移風險並提升檢測能力。

---