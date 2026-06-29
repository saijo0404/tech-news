# Cloud CISO Perspectives: How Google Cloud Security uses AI internally

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-29
- **原文連結**: https://cloud.google.com/blog/products/identity-security/cloud-ciso-perspectives-how-google-cloud-security-uses-ai-internally/

## 核心主題
Google Cloud CISO Chris Betz 與安全工程資深主管 Ruchi Shah 分享 Google 如何將專屬 AI 智能體嵌入軟體開發生命週期（SDLC）各階段，建構自主防禦體系，以對抗機器速度的 AI 驅動威脅。

## 關鍵重點
- **六大 SDLC 智能體防護階段**：從設計審查（以 200+ 項安全需求交叉比對設計文件）、集中化程式碼掃描（Mantis 多智能體架構，以階層式安全摘要樹減少 85% token 用量）、自我修復模糊測試（後設自我反思迴圈解決無狀態 AI 重複犯錯）、統一 AI 修補管線（從復現、上下文映射到自動產生修補程式與回歸測試）、到自主安全姿態管理（ASPM 持續偵測配置漂移），Google 實現了從程式碼 ingestion 到生產環境的全自動化防護。
- **Mantis 架構核心設計**：針對分散式 AI 程式碼掃描準確率低於 7% 的痛點，Mantis 以五大智能體協作——策略智能體評估高階架構、研究智能體深入原始碼、去重/審查/批評智能體過濾誤報、復現沙盒自動執行概念驗證exploit——在保留關鍵結構脈絡的同時將 token 用量減少超過 85%。核心技能已開放原始碼（github.com/google/mantis）。
- **自我反思與持續增強**：Google 引入後設自我反思迴圈（self-reflection loop），由專屬反思智能體分析執行日誌、工具歷史與人類回饋，將成功模式永久儲存至全域知識庫，供未來智能體直接注入上下文，產生「複利效應」，持續提升漏洞修補成功率與效率。

## 結論
Google Cloud 的內部實踐證明，以 AI 規模保護軟體需要從依賴人力的檢查清單轉向自主多智能體協調。結合開放原始碼工具（如 Mantis）與自我修復執行迴圈，Google 正開創「免疫軟體」的未來——應用程式能在即時自我發現、驗證並修補自身弱點，為業界提供了一套可複製的 AI 時代安全防禦藍圖。
