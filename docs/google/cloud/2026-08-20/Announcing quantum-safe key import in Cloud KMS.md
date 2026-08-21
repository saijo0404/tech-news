# Announcing quantum-safe key import in Cloud KMS

- **來源**: Google Cloud Blog
- **發布日期**: 2026-08-21
- **原文連結**: https://cloud.google.com/blog/products/identity-security/announcing-quantum-safe-key-import-in-cloud-kms/

## 核心主題
Google Cloud KMS 正式推出量子安全金鑰導入功能，作為後量子密碼學(PQC)遷移時間表的重要里程碑，幫助企業在量子計算機出現前保護敏感加密金鑰。

## 關鍵重點
- **量子安全 BYOK 能力**：這是 Google Cloud KMS 量子安全功能的首次發布，屬於後量子密碼學遷移時間表的下一步，可幫助企業在量子計算機出現前保護敏感金鑰。
- **混合公開鍵加密(HPKE)**：新的導入方法使用量子抗性的 HPKE 技術，將敏感金鑰材料包裹在量子抗性傳輸信封中，從第一天起就提供量子安全保護。
- **多選演算法支援**：用戶可選擇 X-Wing、ML-KEM-768 或 ML-KEM-1024 等量子安全演算法，並使用 HKDF-SHA-256 進行金鑰派生，最終使用 AES-256-GCM 進行對稱加密。
- **Cloud KMS PQC 洞察**：用戶可透過 Cloud KMS PQC insights 監控整體後量子密碼學狀況，視覺化顯示基於演算法分類的非對稱金鑰，協助規劃未來現代化。

## 結論
這是企業在後量子時代保護敏感金鑰的重要里程碑，透過量子安全金鑰導入功能，企業可以從第一天起就為金鑰提供量子抗性保護，有效抵禦「現在儲存、之後解密」(SNDL)攻擊，並為長期韌性奠定基礎。

---
