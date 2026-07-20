# Level Up Your Column-level Security: Using IAM Data Governance Tags in BigQuery

- **來源**: Google Cloud Blog Data Analytics
- **發布日期**: 2026-07-18
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/level-up-your-column-level-security-using-iam-data-governance-tags-in-bigquery/

## 核心主題
Google Cloud 推出 BigQuery 資料治理標籤預覽功能，提供比傳統策略標籤更強大的欄位級安全性控制方案，支援全域管理、災難復原與階層式分類。

## 關鍵重點
- **資料治理標籤定義**：透過設定 IAM 標籤目的欄位為 DATA_GOVERNANCE 建立，專用於 BigQuery 欄位級安全性，可建立最多五層階級的標籤樹狀結構。
- **全域與區域優勢**：與僅限區域的策略標籤不同，資料治理標籤支援全域範圍設定，可在組織內任何專案或區域使用單一標籤鍵值對。
- **災難復原能力**：安全策略與標籤會自動複製到次要區域，確保災難時安全態勢自動轉移。
- **實施步驟**：
  1. 建立資料治理標籤鍵（設定目的為 DATA_GOVERNANCE）
  2. 建立標籤值並建立階層式樹狀結構
  3. 透過 JSON 模式或 SQL 將標籤附著到欄位
  4. 定義 BigQuery 資料政策以控制存取權限
- **靈活性優勢**：可先分類資料再決定是否強制執行安全策略，提供資料上線期間更多彈性。

## 結論
資料治理標籤是增強 BigQuery 資料安全與治理策略的有力工具，提供可擴展、堅固的欄位級存取控制方案。未來更新將包含更多 SQL 支援功能及與知識目錄的整合。

---

此摘要已儲存至指定檔案路徑。