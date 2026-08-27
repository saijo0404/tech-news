# Using OKF with Knowledge Catalog to serve context for agents

- **來源**: Google Cloud Blog
- **發布日期**: 2026-08-27
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/scale-okf-bundles-across-an-organization-with-knowledge-catalog/

## 核心主題
這篇文章介紹如何使用 Google Cloud 的 Knowledge Catalog 來管理跨組織的 OKF (Open Knowledge Format) bundle，解決知識庫共享和治理問題。

## 關鍵重點
- OKF v0.2 增加了信任信號（來源、驗證、新鮮度、認證），但缺乏跨組織分享與治理機制
- Knowledge Catalog 作為 AI 代理的上下文引擎，將 OKF bundle 映射至現有類型，使每個概念可被發現、治理並被代理讀取
- 技術架構包括 Setup 階段（建立 EntryGroup、EntryType、AspectType）和 Push 階段（每個概念成為 Entry）
- 使用案例：Acme Retail Bundle 包含 9 個葉子概念和 17 個 Entry，展示了完整的 OKF bundle 管理流程
- 主要優勢包括跨組織可發現性、治理、單一 API 呼叫和結構化信號
- 概念查詢機制：透過 LookupContext 查詢 Entry 名稱，返回完整概念體（YAML 格式）
- 收入確認政策 (FY2026) 的定義和實施細節，包括多貨幣訂單換算和核准計算要求
- 權限控制：讀取使用 roles/dataplex.catalogViewer，寫入使用 roles/dataplex.catalogEditor
- 持續導入：CI 工作流在每次提交時呼叫 kcmd push，使用 catalogEditor 權限
- 生命週期管理：kcmd push 為可重複上載，刪除需明確呼叫 kcmd delete 或 cleanup.ts

## 結論
通過將 OKF bundle 導入 Knowledge Catalog，組織可以實現跨組織的知識共享、治理和代理上下文服務，解決了 OKF v0.2 缺乏跨組織管理機制的问题。這使得 AI 代理能夠透過單一 API 呼叫發現、治理和讀取跨組織的知識概念，同時繼承 EntryGroup 的 IAM 權限控制。

---