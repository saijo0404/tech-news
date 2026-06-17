---
# Cloud Network Insights: end-to-end observability for the Cross-Cloud Network

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-17
- **原文連結**: https://cloud.google.com/blog/products/networking/cloud-network-insights-end-to-end-cross-cloud-observability/

## 核心主題
Google Cloud 宣布 Cloud Network Insights 正式通用可用，這是一個與 Broadcom AppNeta 合作打造的雲端原生解決方案，提供跨雲與混合環境的端到端網路可觀測性，讓營運團隊能主動發現並定位效能瓶頸。

## 關鍵重點
- **主動式合成探針與雙層監控**：透過部署輕量級 Monitoring Points 代理程式於關鍵網路區段，持續發送合成流量模擬使用者行為，即使無真實流量也能 24/7 監控。支援網路效能監控（L3/L4，涵蓋 RTT、封包遺失、抖動、路徑變化）與數位體驗監控（L7，含瀏覽器模式使用 Selenium 渲染完整網頁、HTTP 模式輕量級檢查）。
- **智能告警、根因分析與 AI 整合**：自動基線化建立動態效能閾值，異常時即時觸發告警並透過 Cloud Monitoring、Cloud Logging 整合至 Email、Slack 或 PagerDuty；監控政策可根據自訂標籤動態建立或移除路徑；與 Gemini Cloud Assist 整合，以自然語言交叉比對 Cloud Network Insights 指標與其他 Google Cloud 數據，大幅降低平均修復時間（MTTR）。
- **跨雲可見性與客戶驗證**：提供從 Google Cloud、AWS、Azure 到 ISP 與最後一哩連線的單一視圖，打破傳統網路「黑盒子」；Sabre 與 Pexip 等客戶已投入使用，驗證其能將效能瓶頸定位時間從數小時縮短至數秒，並支援 SLA 驗證以確認 ISP 與服務供應商是否符合性能承諾。

## 結論
Cloud Network Insights 將深度網路效能指標與數位體驗監控融合，並直接整合至 Google Cloud Observability 套件與 Gemini AI 能力，為跨雲時代的複雜網路架構提供完整的可觀測性——營運團隊不再需要猜測效能衰退的來源，而是能在第一時間精確定位問題、主動優化體驗。

---
