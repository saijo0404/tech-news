# Shutting the Door on the XCPE Botnet

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-02
- **原文連結**: https://cloud.google.com/blog/topics/threat-intelligence/shutting-the-door-on-the-xcpe-botnet/

## 核心主題
Google 成功摧毀 XCPE 後門駭客網，該後門曾將超過 130 萬機上盒納入控制，並已強化 Android 設備審查機制以預防類似事件。

## 關鍵重點
- **後門開發與獲利模式**：XCPE 後門由 Videostrong Technology 開發，透過出售後門給犯罪同夥並載入惡意軟體模組獲利，獲利模組包括廣告詐騙、住宅代理網路、額外惡意軟體。
- **技術運作機制**：後門運行於系統最高權限，具備重啟後自動恢復能力，使用 MQTT 協議作為 C2 通訊，可遠端安裝軟體、擷取螢幕、執行指令。
- **感染範圍與模組**：主要感染 Android TV 機上盒，包含醫療設備、卡拉 OK 機、數位看板；獲利模組包括 Linkfog、AppSalt、NetNut 等住宅代理，CBOXTV、HiddenView 等廣告詐騙工具。
- **Google 採取行動**：摧毀後門及控制命令(C2)領域，與 Videostrong 斷交，禁止其製造預裝 Google 應用程式設備，並改善 Android 設備審查流程。
- **現代威脅趨勢**：威脅行動者利用雲端資源、LLM 劫持及代理攻擊框架進行牟利，使用 GitHub 儲存庫作為受控頁面發布惡意軟體包。

## 結論
Google 透過此事件成功摧毀 XCPE 後門駭客網，並已強化 Android 生態系的安全審查機制。此事件提醒消費者應警惕「分享頻寬換取報酬」類型的應用程式，硬體製造商也應承擔更多責任。

---