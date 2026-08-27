# Simplify your resilience testing strategy with Fault Injection Testing

- **來源**: Google Cloud Blog
- **發布日期**: 2026-08-27
- **原文連結**: https://cloud.google.com/blog/products/networking/introducing-google-cloud-fault-injection-testing-in-preview/

## 核心主題
Google Cloud 推出 Fault Injection Testing (FIT) 預覽功能，幫助開發者自動測試故障場景，確保服務在高可用性環境中的穩定性。

## 關鍵重點
- 通過故意引入故障來驗證安全機制，確保在實際故障發生前服務能正常運作
- 支持兩種主要故障場景：Cloud SQL 故障轉移和應用流量延遲測試
- 提供乾預模擬功能，可先讀取模擬檢查權限，再手動啟動故障注入
- 建議在預覽期間使用非生產環境，並可通過 Google Cloud 控制台、gcloud CLI 或 REST API 使用

## 結論
這是 Google Cloud 為企業客戶提供的原生故障測試工具，可幫助驗證災難恢復能力並降低服務中斷風險。
---