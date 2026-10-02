# Enabling Cloud Storage end-to-end checksums for improved data integrity and durability

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-02
- **原文連結**: https://cloud.google.com/blog/products/storage-data-transfer/enabling-end-to-end-checksums-in-cloud-storage/

## 核心主題
Google Cloud 現在在 Cloud Storage SDK 中默認啟用端到端校驗和，以確保數據完整性。

## 關鍵重點
- 所有 Cloud Storage SDK 現在默認對上傳數據進行校驗和，並將其傳遞給 Cloud Storage，即使應用程序沒有提供校驗和。
- SDK 支持在下載對象時驗證對象的校驗和。
- 當使用 gRPC API 進行範圍讀取時，SDK 利用 gRPC 內建的端到端範圍校驗和來驗證收到的數據。
- 通過在加密數據後計算校驗和，然後解密並驗證，確保數據完整性。
- 利用循環冗餘校驗(CRC)的屬性，在數據通過多層堆疊時保持校驗和鏈。

## 結論
通過在 SDK 中默認啟用端到端校驗和並在整个内部存储堆栈中保持校驗和鏈，數據從上傳到最終下載保持完整。

---