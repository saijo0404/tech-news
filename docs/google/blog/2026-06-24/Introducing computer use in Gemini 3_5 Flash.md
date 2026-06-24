---
# Introducing computer use in Gemini 3.5 Flash

- **來源**: Google Blog
- **發布日期**: 2026-06-24
- **原文連結**: https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-computer-use-gemini-3-5-flash/

## 核心主題
Google 將 Computer Use 功能原生整合至 Gemini 3.5 Flash 模型，讓開發者能以單一 Flash 級模型建構能在瀏覽器、手機與桌面環境中視覺感知、推理並採取行動的 AI Agent，適用於長程任務與企業自動化場景。

## 關鍵重點
- **從獨立模型到內建工具**：Computer Use 此前僅以獨立 Gemini 2.5 Computer Use 模型提供，現已原生融入 Gemini 3.5 Flash。Gemini 原本就擅長函式呼叫與內建工具（Search、Maps），內建 Computer Use 後，開發者能以 3.5 Flash 可靠地建構自訂 Agent，實現持續軟體測試與跨專業應用知識工作等長程企業自動化任務。可透過 Gemini API 與 Gemini Enterprise Agent Platform 開始使用。
- **安全防範與企業防護機制**：為降低 Live 環境中 Agent 的提示注入風險，Gemini 3.5 Flash 的 Computer Use 採用針對性對抗訓練。Google 同時發布兩項可選企業防護系統：（1）要求對敏感或不可逆操作需明確使用者確認；（2）自動偵測間接提示注入並停止任務。建議結合安全沙盒、人在環路驗證與嚴格存取控制，形成「深度防禦」策略。
- **實際應用與開發資源**：客戶已開始使用 Computer Use 達成價值（例如分析 Gemini 應用並回傳分類功能清單、稽核自身文件的可及性問題）。開發者可透過 Browserbase 託管示範環境測試、參考 GitHub 實作範例，並查看 Gemini API 與 Enterprise Agent Platform 的文件與最佳實踐。

## 結論
將 Computer Use 從獨立模型內建至 Gemini 3.5 Flash，代表 Google 在 Agentic AI 道路上的重要里程碑——開發者不再需要為視覺控制與函式呼叫切換不同模型，單一 Flash 級模型即可處理從簡單工具呼叫到跨平台 Agent 操作的多種場景。配合針對性對抗訓練與企業防護系統，Gemini 3.5 Flash 讓安全且可靠的自主計算操作邁向規模化部署。

---
