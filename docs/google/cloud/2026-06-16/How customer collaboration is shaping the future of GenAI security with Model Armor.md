---
# How customer collaboration is shaping the future of GenAI security with Model Armor

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-16
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/how-customer-collaboration-is-shaping-the-future-of-genai-security-with-model-armor/

## 核心主題
Google Cloud 開發者倡議團隊與電信業客戶共同參與技術衝刺，透過觀察開發者在真實環境中使用 Gemini Enterprise Agent Platform 的痛點，大幅優化 Model Armor（生成式 AI 與代理 AI 執行階段安全服務）的文件與指引。

## 關鍵重點
- **四大開發者痛點洞察**：（1）搜尋優先工作流程——開發者傾向直接搜尋程式碼範例而非閱讀文件層級，缺乏可直接複製貼上的程式碼（如 PII 資料脫敏）造成摩擦；（2）置信度平衡困難——「低及以上」嚴格設定產生大量誤報，干擾正常客服流程；（3）需要更細部的指引——開發者了解核心概念但需要實務執行方法的詳細說明；（4）整合阻礙（403 錯誤）——與 Apigee 等服務整合時頻繁遇到 PERMISSION_DENIED 錯誤，反映文件缺少跨服務 IAM 角色說明。
- **從洞察到行動的具體改善**：新增大量測試過、可直接使用的程式碼範例支援搜尋優先工作流程；推出置信度矩陣（Confidence Level Matrix），建議一般內容使用「高」或「中」閾值以減少誤報，僅在檢測提示注入與越獄等高等級威脅時使用「低及以上」；更新 Apigee、Gemini Enterprise Agent Platform 與 GKE 的整合指南，明確列出所需的 IAM 角色（如 roles/modelarmor.user）；深化執行方法的技術文件說明。
- **「極致同理心」合作模式的力量**：Google Cloud 將與客戶「在同一房間」的觀察視為超越傳統文件循環的獨特價值，透過即時記錄開發者遇到障礙的時刻，將功能阻礙轉化為技術洞察——這種共創模式確保 Model Armor 不只是技術產品，更是真正推動客戶成功的催化劑。

## 結論
Model Armor 的優化過程證明，最好的 AI 安全產品不是闭门造车出來的，而是透過與客戶共同開發、即時觀察真實工作流程、將痛點轉化為具體改善所打造。這種以開發者為中心的協作模式，正重新定義生成式 AI 安全工具的建設方式。

---
