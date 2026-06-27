---
# The Starter Tier for Google AI Studio explained

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-22
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/the-starter-tier-for-google-ai-studio-explained/

## 核心主題
Google Cloud Starter Tier 提供一種簡化的免費開發環境，讓 Google AI Studio 使用者只需一個 Google 帳號即可從提示詞直接部署含資料庫與驗證的全功能 Web 應用程式，無需提供信用卡或設定計費帳戶。

## 關鍵重點
- **預接線的四合一技術堆疊**：Starter Tier 包含 Cloud Run（無伺服器運算，最多同時部署兩個應用程式）、Firebase Authentication（內建 Google Sign-In）、Cloud Firestore（NoSQL 資料庫，1 GiB 儲存、每日 40,000 寫入 / 50,000 讀取共享配額）與 Cloud SQL for PostgreSQL Developer edition（支援 pgvector 的關聯式資料庫）。所有資源由 Google 全權管理，使用者只需描述需求、點擊發布即可獲得 .run.app 網址，全程無需 Dockerfile、gcloud CLI 或 YAML 設定檔。
- **與 Free Trial 的差異與使用限制**：Starter Tier 專為 AI Studio 原型開發設計，與需信用卡、有 90 天期限的 Free Trial 不同，它沒有時間限制且專案由 Google 托管，但功能受限——無法啟用 BigQuery、Pub/Sub 等額外 API，所有資源鎖定於單一區域，且檔案系統為暫存性（容器縮至零時資料會消失）。Firestore 所有資料庫共享單一配額群組，任一資料庫耗盡配額時整個群組會暫停至太平洋時間午夜。
- **無縫升級至完整 Google Cloud**：升級時無需遷移、匯出資料或更改 DNS。使用者在 AI Studio 專案頁面設定計費並輸入信用卡後，即可原地升級至付費方案，Cloud Run 服務持續運作、資料庫資料保留、.run.app 網址不變。升級後獲得完整 IAM 控制與所有 API 存取權。建議設定預算警報、Cloud Run 最大實例上限與 API 調用配額以防止意外費用。注意 Firestore 資料庫升級後仍需至 Firebase 控制台中點擊「升級資料庫」以解除共享配額群組。

## 結論
Google Cloud Starter Tier 是連接 AI 原型與生產部署之間最短的路徑——從提示詞到上線網址只需五個步驟，讓開發者能快速驗證想法而不必擔心基礎設施。其無縫升級設計確保原型可以原封不動地成長為生產級應用，大幅降低了從構想到產品的技術門檻。

---
