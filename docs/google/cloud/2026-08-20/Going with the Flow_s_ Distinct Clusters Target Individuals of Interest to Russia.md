# Going with the Flow(s): Distinct Clusters Target Individuals of Interest to Russia

- **來源**: Google Cloud Blog
- **發布日期**: 2026-08-21
- **原文連結**: https://cloud.google.com/blog/topics/threat-intelligence/distinct-clusters-target-individuals-of-interest-to-russia/

## 核心主題
Google 安全團隊追蹤到三個俄羅斯網絡間諜群組，利用合法認證流程（如應用程式密碼、OAuth）針對俄羅斯感興趣的個人進行釣魚和惡意軟體攻擊。

## 關鍵重點
- **UNC6293**：被評估為 ICE RELIC (前 APT29) 子群組，專注於初始訪問操作，使用應用程式密碼釣魚和 OAuth 釣魚，偽裝美國國務院
- **UNC7005**：技術較不成熟，使用 VIDAR、ATOMIC 等惡意軟體，針對烏克蘭、西歐及美國人員進行攻擊，使用設備代碼釣魚
- **UNC5976**：專注於 OAuth 釣魚技術與自動化 token 收集，分發 HEADRUSH 惡意 Excel 插件，目標集中在烏克蘭航空航天與成像公司
- **共同特徵**：均利用 OAuth 技術進行身份驗證竊取，持續適應性釣魚活動，攻擊者會修改操作以逃避自動分析
- **Google 建議**：不繼續可疑網站警告，檢查 URL 並透過官方管道驗證邀請，避免使用應用程式密碼，撤銷舊密碼，警惕郵件/訊息中的偽裝身分

## 結論
這些俄羅斯間諜群組利用合法認證流程進行攻擊，使追蹤合法與惡意帳號存取變得困難。企業應提高警覺性，強制註冊鎖定與雙因素認證、定期審查裝置連結，並利用安全數字/代碼進行驗證。

---