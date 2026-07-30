# Automate your agent development lifecycle using any coding agent

- **來源**: Google Cloud Blog Developers & Practitioners
- **發布日期**: 2026-07-30
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/automate-agent-development-lifecycles-with-gemini-enterprise/

## 核心主題
這篇文章介紹了如何使用 Gemini Enterprise Agent Platform 和 Agents CLI，透過單一提示（prompt）就能完成整個代理（agent）開發生命週期，從設定、建置、部署、治理、評估到發布，無需在不同工具之間切換。

## 關鍵重點
- 使用 Agents CLI 技能套件，讓編碼代理能自動完成代理開發生命週期的所有階段，包括設定、建置、部署、治理、評估和發布
- 以「Industry Watch」代理為例，展示如何建置一個能比對半導體公司新聞稿與 SEC 文件的競爭情分析工具，解決大模型無法追溯來源的問題
- 強調架構設計的重要性：透過確定性工具（如 SEC 數據抓取、新聞比對）來確保答案可追溯，避免大模型胡編亂造
- 治理與安全：透過 Agent Identity、Agent Registry、Agent Gateway 和 Model Armor 等工具，確保代理身份權限最小化、網路訪問受控、並防護提示注入攻擊
- 評估機制：建立基於真實數據的評估集，以具體指標（如引用編號是否正確）來衡量代理質量，並納入 CI 流程
- 發布到 Gemini Enterprise：將代理發布到企業應用中，讓業務用戶可直接使用，無需 SSH 登入

## 結論
透過提示工程（prompt engineering）和自動化工具，開發者可以輕鬆構建可生產化、可治理、可評估的企業級代理，無需手動切換多個平台或工具。Industry Watch 代理只是其中一個範例，這種模式適用於任何需要即時數據、可驗證答案和受控工具邊界的任務。

---