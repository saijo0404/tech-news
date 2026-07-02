---
# Google's Continued Disruption of Malicious Residential Proxy Networks

- **來源**: Google Cloud Blog
- **發布日期**: 2026-07-02
- **原文連結**: https://cloud.google.com/blog/topics/threat-intelligence/google-continued-disruption-residential-proxy-networks/

## 核心主題
Google 與 FBI、Lumen 等單位協調，對全球大型住宅代理網路 **NetNut（又稱 Popa）** 發動新一輪打擊行動——透過禁用惡意 C2 帳號、共享技術情資、啟用 Google Play Protect 自動攔截，使該代理網路可用裝置數量暴減数百万台。

## 關鍵重點
- **NetNut 規模與運作模式**：GTIG 估計 NetNut 至少控制 **200 萬台裝置**遍布全球，透過在智慧電視、串流盒子等家用裝置上預裝或隱含 SDK 來建立僵尸網路。NetNut 同時販售品牌服務與白牌授權（reseller program），Google 高度懷疑許多知名住宅代理品牌實際上是白牌轉售 NetNut 僵尸網路。操作者會因自身網路受挫而購買競爭對手容量，形成「互為轉售」的連動生態。
- **對攻擊者的戰略價值與消費者風險**：2026 年 6 月單週內，GTIG 观察到 **316 個不同威脅叢集**（含網路犯罪與間諜組織）使用 NetNut 出口節點進行攻擊——包括掩護來源 IP、密碼噴射攻擊、存取受害者環境等。更嚴重的是，當家用裝置成為出口節點時，未經授權的網路流量會經過該裝置，攻擊者可藉此存取同一家庭網路中的其他私人裝置，並有報告指出 NetNut 被用於傳播 Mirai DDoS 僵尸網路變種。
- **Google 的三重打擊與消費者保護建議**：①**停用 C2 基礎設施**——禁用 NetNut 用於惡意命令控制的 Google 帳號與服務。②**生態系協同**——共享 NetNut SDK 與後端 C2 情資給平台供應商、執法單位與研究機構。③**Play Protect 自動防護**——Android 內建安全防護自動警告並停用含 NetNut SDK 的應用程式。Google 警告消費者應遠離任何以「分享剩餘頻寬」為名付款的應用程式，並只從官方管道購買連線裝置。

## 結論
住宅代理網路產業正快速擴張，操作者之間互相依賴、重疊的僵尸網路形成一個「打不死」的流動生態——單一打擊只能造成暫時性破壞，持續且協調的跨平台行動才是長期解方。Google 明確表示這不是最後一次行動，並呼籲行動平台、ISP 和其他科技平台持續共享情資、直接阻斷惡意 C2 基礎設施，以共同遏制這項威脅。

---
