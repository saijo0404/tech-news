---
# How Siemens "slices the elephant" advancing agentic workflows for industrial software development

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-16
- **原文連結**: https://cloud.google.com/blog/products/ai-machine-learning/how-siemens-sliced-the-elephant-modernizing-legacy-code-with-agentic-workflows/

## 核心主題
Siemens 與 Google Cloud 合作打造 Knowledge Fabric——一個結合 Spanner Graph 知識圖譜與 Gemini、Claude Code 等 AI 模型的智慧代理系統，協助 Siemen 將數億行 legacy 程式碼進行現代化改造，同時保持工業級軟體的嚴格品質與合規要求。

## 關鍵重點
- **四大挑戰與知識圖譜解決方案**：Siemens 面臨程式碼規模龐大（超出標準 LLM 上下文視窗）、知識碎片化（散佈於程式碼、Jira、Confluence 與 2000 年代掃描 PDF）、複雜度（追溯十年前的功能需求文件）、以及嚴格合規責任。團隊以 Spanner Graph 建立程式碼結構的知識圖譜，結合嵌入向量搜尋（ANN）與全文檢索，讓代理系統能以 Graph Query Language（GQL）遍歷依賴關係，回答如「修改 Axis Control Panel 的邏輯會影響哪些函式」等複雜查詢。
- **「切象法」代理工作流程**：團隊發現 AI 代理難以處理龐大模糊任務，因此將「重構此模組」等廣泛請求拆解為五個專門代理的有序步驟：（1）搜尋代理——深度探索程式碼圖譜並交叉比對文件；（2）使用者故事代理——與產品負責人對話以收集需求並撰寫詳細使用者故事；（3）架構影響代理——分析圖譜預測變更的副作用；（4）任務拆解代理——將分析結果轉為可執行的小任務；（5）程式碼代理——在充分脈絡下實現變更。每個步驟均有工程師參與監督。
- **試產成果與生產效益**：以往需要資深工程師花數天分析依賴關係的工作，現在大幅縮短。在近期將 legacy 控制面板遷移至現代化網頁介面的試產案中，Knowledge Fabric 在維持系統完整性與工業品質標準的同時，顯著降低了整體程式碼工作量，讓工程師能將時間投入到創造客戶價值而非重複性實作。

## 結論
Knowledge Fabric 證明生成式 AI 不僅能編寫样板代碼，更能協助企業現代化最關鍵的 legacy 系統。透過知識圖譜提供結構化脈絡、代理工作流程將大任務拆解為可管理步驟、以及人類在環的監督機制，Siemens 為工業軟體的 AI 現代化樹立了新典範——讓工程師從重複勞動中解放，專注於更高價值的問題解決。

---
