# The Blueprint: How Kult built a gaming companion that actually knows your game

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-20
- **原文連結**: https://cloud.google.com/blog/products/gaming/kult-built-a-gaming-companion-with-gemini-that-actually-knows-your-game/

## 核心主題
Kult 使用 Google Gemini 模型系列建立了一個遊戲伴侶系統，能根據玩家當下的遊戲狀態提供即時、準確的遊戲資訊，解決了傳統遊戲求助方式中斷沉浸感的問題。

## 關鍵重點
- **多模型架構**：使用 Gemini 模型系列（Flash 和最新模型）根據任務複雜度動態匹配，平衡性能、速度和成本
- **自動化知識庫**：每款遊戲建立自動更新的結構化知識庫，支持 100+ 遊戲，新增遊戲無需手動工作
- **雙重輸出體驗**：語音提供簡短回答，同時在第二螢幕展示視覺化內容（圖片、視頻、地圖、互動工具）
- **個性化答案**：根據玩家遊戲進度（10 分鐘內 vs 100 小時經驗）提供不同層次的回答
- **決策優化**：使用 Jev 決策模型快速處理簡單查詢，複雜問題才調用大型模型，降低成本

## 結論
Kult 展示了如何利用 Google Cloud 技術（Gemini 模型系列、GKE 架構、Live 模型）建立可擴展的遊戲伴侶系統，並正在 Alpha 測試階段。未來將擴展至電腦視覺功能，讓遊戲伴侶能主動感知遊戲畫面。

---