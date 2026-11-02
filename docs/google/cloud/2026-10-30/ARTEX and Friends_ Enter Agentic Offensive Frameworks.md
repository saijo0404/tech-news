# ARTEX and Friends Enter Agentic Offensive Frameworks

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-30
- **原文連結**: https://cloud.google.com/blog/topics/threat-intelligence/artex-and-friends-enter-agentic-offensive-frameworks/

## 核心主題
Google Threat Intelligence Group 與 Mandiant 發現攻擊者開始使用 ARTEX、Hexstrike 和 CAIRN 等開源多代理攻擊框架，標誌著威脅演進的關鍵轉折點。自主攻擊框架因低門檻、易整合、規模化潛力而具吸引力，但會留下更多痕跡。

## 關鍵重點
- **ARTEX 框架特性**：Go 語言撰寫的自動化多代理 LLM 驅動攻擊平台，包含六個專業子代理，攻擊速度從數小時縮短至 15 分鐘內完成完整攻擊週期
- **攻擊演進階段**：從 Stage 1 (基於提示的 LLM 使用) 到 Stage 7 (高階、完全自主/代理攻擊)，目前處於 Stage 5 (多階段攻擊由 LLM 驅動工具執行)
- **五層防禦策略**：保護控制平面、限制身份與金鑰、硬化配置、應用保護、檢測行為變化
- **四層防禦措施**：Layer 1 保護控制平面、Layer 2 限制身份與金鑰、Layer 3 強化配置並減少攻擊路徑、Layer 4 強化應用程式開發
- **高風險操作管控**：用戶、權限修改等高影響操作應設定速率限制、收件人限制、交易門檻及濫用控制
- **行為與體積變化偵測**：建立正常行為基準，監控認證來源變化、管理 API 呼叫速度、資料平面活動等

## 結論
自主攻擊框架正改變威脅演進，攻擊者利用低門檻工具縮短攻擊時間並增加欺骗性。防禦需結合控制與監控，實施長期安全最佳實踐，包括控制平面隔離、短期憑證、最小權限原則及網路分段。

---