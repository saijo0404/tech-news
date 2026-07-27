# Open Knowledge format v0.2 tackles agentic trust

- **來源**: Google Cloud Blog
- **發布日期**: 2026-07-25
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/okf-v0-2-adds-trust-signals/

## 核心主題
Google 推出 Open Knowledge Format (OKF) v0.2，透過新增信任信號（provenance, trust, freshness, lifecycle, attestation）來解決 AI 代理生成內容的可信度問題。

## 關鍵重點
- **五問機制**：OKF v0.2 新增五個關鍵問題的答案機制：來源（provenance）、信任（trust）、新鮮度（freshness）、生命週期（lifecycle）、認證（attestation），讓消費者能明確判斷內容的可信度。
- **新增 frontmatter 欄位**：引入 generated（生成資訊）、verified（驗證記錄）、status（狀態）、stale_after（過期日期）、sources（來源）、attestation（認證計算）等欄位，用於在讀取內容前進行決策。
- **Attested Computation 概念類型**：新增可驗證的計算類型，記錄可驗證的計算過程，確保數值符合規範，並透過 attester 機制驗證計算結果。
- **信任分級機制**：建立信任分級（無驗證=未驗證、機器驗證=機器確認、人類驗證=人類審查），讓消費者可透過信任分級過濾內容。
- **最小化原則**：新增欄位皆為可選，不採用任何新增的格式仍完全有效，保持格式的最小化原則。

## 結論
OKF v0.2 是相容性升級，不強制採用，但讓消費者能透過信任信號過濾內容，提升 AI 代理生態的可信度。未來將鼓勵更多開發者採用信任信號，使 OKF 成為更廣泛使用的標準化格式。
---
