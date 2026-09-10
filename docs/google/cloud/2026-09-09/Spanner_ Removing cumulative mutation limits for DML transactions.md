# Spanner Removes Cumulative Mutation Limits for DML Transactions

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-10
- **原文連結**: https://cloud.google.com/blog/products/databases/spanner-removes-dml-mutation-limits/

## 核心主題
Google Cloud Spanner 移除了 DML 操作的累積突變限制，允許單一交易包含更多 DML 語句，提供更靈活的資料一致性解決方案。

## 關鍵重點
- **限制變更方式**: 原先的 80,000 突變限制從交易層級改為個別 DML 語句層級，單一交易可包含任意數量的 DML 語句（只要每個語句個別未超過 80,000 突變）。
- **主要優勢**: 應用程式可根據業務需求邏輯分組 DML 語句，無需因限制而人工拆分交易，且無需更新現有應用程式代碼。
- **技術注意事項**: 雖然可包含更多 DML 語句，但較長的交易會持有鎖定更久，可能增加鎖定競爭和交易中止的風險。

## 結論
此更新為開發者提供了更大的靈活性，可運行更大規模的交易，同時利用 Spanner 的全球一致性，無需犧牲一致性、可擴展性或可用性。

---