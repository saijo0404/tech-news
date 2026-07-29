# Future-proofing data integrity: Quantum-safe digital signatures in Cloud KMS

- **來源**: Google Cloud Blog Security & Identity
- **發布日期**: 2026-07-29
- **原文連結**: https://cloud.google.com/blog/products/identity-security/future-proofing-data-integrity-quantum-safe-digital-signatures-in-cloud-kms/

## 核心主題
Google Cloud KMS 正式推出量子安全數位簽章（ML-DSA、SLH-DSA）和後量子鍵封裝（ML-KEM），以應對量子電腦威脅，確保長期資料完整性與真實性。

## 關鍵重點
- **多種 PQC 演算法支援**：提供 ML-DSA-44、ML-DSA-65、ML-DSA-87 和 SLH-DSA-SHA2-128s 等演算法，支援 Level 1 至 Level 5 不同安全等級，符合 NIST FIPS 204/205 標準。
- **外部-hash 與 external-µ 變體**：解決大資料載體簽名時的頻寬和處理問題，應用程式可先在本地計算固定大小的摘要（digest），再傳送給 KMS 進行簽名，實現高效能、低延遲的簽名工作流。
- **非重新簽名性保障**：external-µ 變體將公開金鑰數學上綁定至訊息摘要，防止攻擊者 manipulates 訊息摘要以在不同金鑰下驗證。
- **易於整合**：開發者可透過 Cloud KMS API 使用現有功能創建、管理並使用 PQC 金鑰進行簽名操作，詳細說明和程式碼範例可在 KMS 文檔中找到。
- **持續更新承諾**：Google Cloud 承諾持續更新服務以納入未來 NIST 標準和指引，協助客戶維持系統安全性。

## 結論
Google Cloud KMS 推出量子安全數位簽章是後量子遷移的重要里程碑，幫助組織進行量子安全遷移策略。隨著量子電腦威脅日益嚴重，這項功能讓企業能夠主動應對未來安全挑戰，確保長期資料完整性。

---