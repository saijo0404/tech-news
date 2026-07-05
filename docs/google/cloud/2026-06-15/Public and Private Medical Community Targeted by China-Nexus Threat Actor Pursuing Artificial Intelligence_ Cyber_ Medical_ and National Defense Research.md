# Public and Private Medical Community Targeted by China-Nexus Threat Actor Pursuing Artificial Intelligence, Cyber, Medical, and National Defense Research

- **來源**: Google Cloud Threat Intelligence Blog
- **發布日期**: 2026-06-16
- **原文連結**: https://cloud.google.com/blog/topics/threat-intelligence/prc-targets-us-medical-research/

## 核心主題
Google 威脅情報小組（GTIG）揭露中國背景威脅組織 UNC6508 自 2023 年 9 月起，針對北美國立、州立及私立醫學研究機構進行長期間諜活動，利用 REDCap 伺服器漏洞植入惡意軟體 INFINITERED，偷取 AI、網路、醫療及國防研究等敏感資料。

## 關鍵重點
- **廣泛的情報收集與創新外洩手法**：UNC6508 瞄準地緣戰略政策、軍事戰略、先進技術與醫療研究（包含 2025 年廣東省爆發的齊卡古尼亞熱病原體），並首次被觀察到使用「網域內容合規規則」濫用技術——建立名為「Patroit」的合規規則，將匹配的郵件靜密 BCC 轉寄至其控制的 Gmail 帳號進行資料外洩。
- **先進的持久化惡意軟體 INFINITERED**：該組織利用 REDCap 舊版軟體漏洞取得立足點後，部署三模組惡意軟體——透過 GUID 分隔符號從升級檔中提取惡意程式碼實現升級攔截、在登入過程中截獲帳號密碼加密隱藏於合法資料庫表中、以及透過全域 hooks 等待特定 Cookie 參數執行系統指令與 SQL 查詢，全程使用美國 IP 與欺騙網絡（OBF networks）掩護。
- **全面防護建議**：GTIG 建議企業對管理員帳戶強制實施防釣魚的 2SV、部署進階保護計畫、啟用裝置綁定工作階段憑證（DBSC）、全面更新並移除舊版 REDCap、使用 YARA 規則掃描 INFINITERED、審計合規規則變更，並將 Workspace 日誌納入 SIEM 管線監控。

## 結論
UNC6508 展示了國家背景黑客組織如何透過精心設計的持久化技術與創新資料外洩手法，長期瞄準醫療與國防研究領域的高價值情報。Google 已與 Mandiant Consulting 合作中斷該組織基礎設施並通知受影響機構，此案提醒醫療與學術機構即使是常用的研究工具也可能成為高級威脅的切入點，全面的安全防護與持續監控至關重要。

---
