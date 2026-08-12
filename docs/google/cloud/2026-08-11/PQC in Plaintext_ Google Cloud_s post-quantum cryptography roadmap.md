# PQC in Plaintext: Google Cloud's post-quantum cryptography roadmap

- **來源**: Google Cloud Blog
- **發布日期**: 2026-08-12
- **原文連結**: https://cloud.google.com/blog/products/identity-security/pqc-in-plaintext-google-clouds-post-quantum-cryptography-roadmap/

## 核心主題
Google Cloud 宣布其後量子密碼學 (PQC) 遷移路線圖，目標於 2029 年實現全面 PQC 準備，涵蓋三個關鍵領域：SNDL 風險緩解、完整性與非否認性、以及基礎設施能力增強。

## 關鍵重點
- **2026 年立即進展**: API 端點已提供量子安全鍵交換，負載平衡器支援量子安全混合鍵交換，Cloud KMS 已推出 NIST 標準化 PQC 演算法。
- **2027-2028 年核心領域**: 針對 SNDL 風險、數位簽章完整性、以及基礎鍵管理建立具體遷移路線圖。
- **2029 年全面準備**: 預計 2029 年達成全面 PQC 準備，並持續至 2030 年代以配合 CNSA 2.0 及 NIST IR 8547 標準。
- **客戶責任**: 組織需自行管理應用程式更新、客戶端軟體 PQC 演算法支援，以及更新 Google Cloud 服務配置。

## 結論
Google Cloud 透過風險優先方法論，分階段推動 PQC 遷移，強調客戶與 Google 的共同責任。建議客戶立即開始：清查加密資源、更新開發工具、並驗證現有應用程式行為。

---