# BGP route policies_ Top 3 use cases by customer demand

- **來源**: cloud.google.com/blog
- **發布日期**: 2026-07-08
- **原文連結**: https://cloud.google.com/blog/products/networking/bgp-route-policies-top-3-use-cases-by-customer-demand/

## 核心主題
這篇文章介紹了 Google Cloud BGP route policies 的三大主要客戶使用案例，包括路徑過濾與網路保護、影響流量路徑的 active/standby 架構，以及透過 BGP 社群解決非對稱路由問題。

## 關鍵重點
- **路徑過濾與網路保護**：使用 BGP route policies 建立「fail closed」環境，透過「drop all」策略確保絕對的網路路由控制，防止路由迴圈和流量劫持
- **流量路徑影響**：透過動態修改 BGP multi-exit discriminator (MED) 屬性或 AS-PATH prepending，在不修改本地硬體的情況下影響首選路徑，優化成本或管理 active/standby 連接
- **非對稱路由解決方案**：透過 BGP 社群標籤匹配，確保返回流量從相同的防火牆或網路設備返回，解決需要狀態式防火牆的企業網路問題

## 結論
透過 BGP route policies 和 Common Expression Language (CEL)，企業可以更靈活地管理混合雲端連接性，優化網路路由策略並增強安全性，建議在生產環境前先在測試環境驗證 CEL 表達式和路由邏輯。

---
