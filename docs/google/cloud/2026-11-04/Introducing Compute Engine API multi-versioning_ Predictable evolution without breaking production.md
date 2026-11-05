# Introducing Compute Engine API multi-versioning: Predictable evolution without breaking production

- **來源**: Google Cloud Blog Developers & Practitioners
- **發布日期**: 2026-11-05
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/introducing-compute-engine-api-multi-versioning-predictable-evolution-without-breaking-production/

## 核心主題
Google Cloud 推出 Compute Engine API 多版本化功能，透過日期基礎的 API 版本讓開發者可以安全地升級 API，同時保持生產環境的穩定性。

## 關鍵重點
- **日期基礎的 API 版本化**：取代原有的通道基礎版本化，引入 Stable（穩定版）和 Preview（預覽版）兩種日期基礎版本，每個版本都是不可變的合約。
- **自主控制升級時間**：開發者可以自主決定何時升級 API 版本，將升級風險限制在測試環境，完全控制升級節奏。
- **更安全與更現代化的 API**：新版本提供更強的韌性預設值（如全域查詢自動啟用部分成功）、可行動的機器可讀錯誤訊息（符合 AIP-193 標準），以及更安全的 IAM 權限檢查。
- **無縫兼容現有工具**：SDK、gcloud CLI、Terraform 等客戶端工具自動支援多版本化，無需修改現有代碼或重新編寫整合。

## 結論
這項功能讓 Google Cloud 可以在不影響生產環境穩定性的前提下，持續改進 API 功能，為開發者提供更現代化、更安全且更易於自動化的 API 體驗，同時解決了長期 API 穩定性與持續改進之間的矛盾。
---
