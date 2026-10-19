# Investigating Ephemeral Supply Chain Tampering

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-15
- **原文連結**: https://cloud.google.com/blog/topics/threat-intelligence/investigating-ephemeral-supply-chain-tampering/

## 核心主題
Google Threat Intelligence Group (GTIG) 與 Mandiant 調查到 2026 年 4 月至 7 月間，威脅群組 UNC7017 針對 AOMEI Technology 更新基礎設施發動供應鏈攻擊，透過短暫的伺服器配置篡改利用合法更新機制分發惡意軟體。

## 關鍵重點
- **攻擊手法**：攻擊者利用 AOMEI 更新機制進行側載攻擊，透過 Radmin 3.x 管理套件分發 SHINYROAD 模組化後門框架，並使用 BlkScrDl.dll 劫持 Radmin 啟動過程。
- **惡意軟體**：主要包含 CROSSROAD 下載器、SHINYROAD 後門框架、ADAPTAGENT 後利用載入器，以及多個偽裝載體（NitroPromotion.exe、Nitro_Scan2PDFApp.exe）。
- **C2 基礎設施**：攻擊者利用多個 C2 IP（8.210.84.56、8.218.65.184、47.239.60.117）及惡意域名（storage-data.com、promotion.storage-data.com），並利用 Alibaba Cloud OSS 和 Google Cloud Storage 作為緩存伺服器。
- **受害者範圍**：涵蓋澳洲、巴西、印度等多個國家，涉及 IT 服務、電信、高等教育等領域，受害者透過 Zoho 的 ManageEngine Threat Analysis Lab (METAL) 偵測並通報。
- **MITRE ATT&CK 技術**：包含供應鏈 compromise (T1195.002)、命令與控制 (T1105)、持久化 (T1053.005)、執行防護 (T1480)、偽裝 (T1036.005) 等技術。

## 結論
此供應鏈攻擊案例展示了攻擊者利用合法更新機制進行側載攻擊的危險性，組織應實施端到端加密簽名驗證、數位簽名配置檔案及來源完整性監控，並進行端點與網路獵檢以清除已下載的惡意更新。

---