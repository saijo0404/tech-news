# BGP route policies: Top 3 use cases by customer demand

- **來源**: Google Cloud Blog
- **發布日期**: 2026-07-08
- **原文連結**: https://cloud.google.com/blog/products/networking/bgp-route-policies-top-3-use-cases-by-customer-demand/

## 核心主題
Google Cloud Router 的 BGP route policies 功能已推出超過一年，客戶利用此功能建立了複雜且具韌性的路由架構。今年推出的 Policy named sets 進一步簡化了配置管理。

## 關鍵重點
- **Route filtering 與網路保護**: 客戶廣泛使用 BGP route policies 過濾不需要的學習路徑，並透過添加 "drop all" 策略建立 "fail closed" 環境，防止路由循環和 BGP hijack。
- **影響流量路徑以實現主動/備用架構**: 透過動態修改 BGP MED 屬性或 AS-PATH prepending，讓網路團隊在不觸碰本地硬體的情況下影響預選路徑。
- **使用 BGP communities 解決非對稱路由**: 透過在本地標記特定 BGP communities，Cloud Router 可調整路徑偏好，確保回傳流量以對稱方式流動，解決使用狀態型防火牆或網路設備時的流量對稱性問題。

## 結論
使用 BGP route policies 優化並 sécurize 您的混合雲端連接性比以往更容易、更堅固。建議在 staging 環境測試 CEL 表達式和路由邏輯，再上線至生產環境。

---

*此摘要已儲存至指定檔案路徑。*
