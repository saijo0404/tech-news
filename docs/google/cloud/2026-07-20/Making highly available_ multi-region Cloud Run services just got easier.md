# Making highly available, multi-region Cloud Run services just got easier

- **來源**: Google Cloud Blog
- **發布日期**: 2026-07-20
- **原文連結**: https://cloud.google.com/blog/products/serverless/cloud-run-multi-region-services-enhanced-for-high-availability/

## 核心主題
Google Cloud 推出了增強的 Cloud Run 多區域服務功能，使建立高可用性、多區域服務變得更加簡單。

## 關鍵重點
- 準備性探針（Readiness probes）提供實例層級的健康檢查，可精確判斷容器是否準備好服務流量
- 服務健康（Service health）聚合實例層級的健康檢查，計算每個區域的服務健康狀況，並透過 serverless 網路端點群組（NEGs）暴露
- 當服務連接到全域外部應用程式負載平衡器時，流量會自動從不健康的區域轉移

## 結論
這些新功能讓建立高可用性、多區域的 Cloud Run 服務變得更加簡單，且目前所有區域都免費提供，只需支付標準 CPU 和記憶體費用。
---