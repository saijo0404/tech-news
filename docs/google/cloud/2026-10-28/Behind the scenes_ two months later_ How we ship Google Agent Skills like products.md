# Behind the scenes, two months later: How we ship Google Agent Skills like products

- **來源**: Google Cloud Blog Developers & Practitioners
- **發布日期**: 2026-10-29
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/behind-the-scenes-two-months-later-how-we-ship-google-agent-skills-like-products/

## 核心主題
這篇文章分享了 Google Agent Skills 項目在過去兩個月內如何像產品一樣發布技能，包括自動化質量閘門、AI 審查代理以及從中獲得的教訓。

## 關鍵重點
- **核心哲學**：將技能更新視為產品發布，而非一次性文檔。技能是 AI 代理的推理循環、工具選擇和執行路徑的指南，而非僅供人類閱讀的文檔。
- **自動化質量閘門**：每個技能變更必須通過六個自動化檢查（結構合規性、技能檢查器、語義版本控制、評估套件、連結驗證、AI 審查代理）和人類審查。
- **語義版本控制**：每個行為變更都需要明確的版本升級，新技能從 1.0.0 開始，升級時遵循標準重置規則（升級 MAJOR 時重置 MINOR 和 PATCH，升級 MINOR 時重置 PATCH）。
- **評估套件驗證**：確保評估套件正確無誤，包括文件引用解析、原子化期望、重複檢測和強制評估報告。
- **AI 審查代理**：使用 AI 審查技能來評估技能質量，包括技能適配性、L1/L2/L3 模塊化架構和非互動式腳本設計。
- **人類審查**：所有拉取請求必須獲得人類審查員（通常是領域專家）的批准。

## 結論
這些自動化質量閘門和審查規則可以應用於任何技能存儲庫，以確保技能的高質量和一致性。Google Agent Skills 項目已累積超過 21,000 個 GitHub 星號，並分佈於多個 AI 平台。

---