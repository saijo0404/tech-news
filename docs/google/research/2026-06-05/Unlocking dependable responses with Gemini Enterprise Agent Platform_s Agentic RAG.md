# 使用 Gemini Enterprise Agent Platform 的代理式 RAG 解鎖可靠回應

- **來源**: Google Research Blog
- **發布日期**: 2026-06-05
- **原文連結**: https://research.google/blog/unlocking-dependable-responses-with-gemini-enterprise-agent-platforms-agentic-rag/

## 核心主題
Google 推出 Gemini Enterprise Agent Platform 支援的代理式檢索增強生成（Agentic RAG），以多代理架構與創新「充足情境」（Sufficient Context）檢查機制，解決傳統 RAG 在跨來源、多跳躍查詢中資訊斷鏈的問題，將事實準確率提升高達 34%。

## 關鍵重點
- **多代理架構模擬研究部門**：系統將複雜查詢拆解為五大角色——協調員（Orchestrator）評估需求並委派、規劃員（Planner Agent）繪製資訊路徑、查詢重寫器（Query Rewriter）將模糊提問轉為精準搜尋詞、搜尋分發員（Search Fanout Agent）向多來源收集片段、最後由 LLM 整合生成回答；以醫生查詢病患出院藥物、飲食與過敏史的案例展示跨三個獨立資料庫（藥房、營養、臨床筆記）的完整流程。
- **充足情境 Agent：核心創新與迭代搜尋**：創新「充足情境 Agent」扮演品質檢查員角色，在生成回答前逐項驗證三項內容——實際檢索到的文字片段、系統草稿回答、以及缺失項目分析；當發現缺失時不只回傳「資訊不足」，而是產生具體的 Reason 與 Feedback（如「有藥物與飲食資料但缺少過敏反應，請搜尋 rashes 或 adverse events」），觸發查詢重寫器重新搜尋，直到所有資訊完整才允許 Synthesis Agent 輸出最終答案。
- **FramesQA 實驗與跨語料庫表現**：在 FramesQA 基準測試（824 筆多跳躍查詢、2,676 份 PDF）中，系統於跨語料庫設定下（需從 4 個不相關數據集中選擇正確來源並混入三個干擾數據集）仍以 90.1% 正確率接近單一語料庫表現，且兩者延遲差異僅約 3%，證明系統能在多個無關數據源上可靠推理，同時維持一致效能。

## 結論
透過進階查詢規劃、路由與充足情境檢查的結合，Google 的代理式 RAG 確保 AI 生成回應可審計、可追蹤且扎根於事實，目前已以公開預覽形式開放於 Gemini Enterprise Agent Platform，為企業級 AI 系統建立新的可靠標準。
