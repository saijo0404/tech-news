# How to Evaluate AI Agents From Tool Calls to Task Completion

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-09-21
- **原文連結**: https://developer.nvidia.com/blog/how-to-evaluate-ai-agents-from-tool-calls-to-task-completion/

## 核心主題
AI Agent 評估已從單一函數呼叫評分轉變為測量完整任務完成度，透過可執行環境追蹤跨多步驟工具使用的狀態。

## 關鍵重點
- **雙層評分機制**：步驟級評分（process scoring）識別鏈條斷裂點，端到端評分（E2E）驗證最終環境狀態是否達成目標。
- **核心指標架構**：評估透過固定層級架構（Benchmark → Trial → Task → Turn → Step）滾動，包含準確率、冗長度和成本三個軸。
- **可執行驗證優先**：可執行檢查（如資料庫更新、測試通過）是金標準，優於參考基準或 LLM 作為評審方法。
- **Nemotron 3.5 Lightning 表現**：在 PinchBench 上達到 86% 準確率，完成任務速度快 30%。
- **企業部署建議**：應優先採用基於真實工單和 API 的領域特定評估，以環境狀態為閘控條件而非孤立呼叫準確性。

## 結論
企業部署 AI Agent 時，應將評估重點放在任務完成度和環境狀態變化上，而非單一函數呼叫的準確性。透過可執行驗證和雙層評分機制，能更準確地評估模型在真實環境中的表現。

---