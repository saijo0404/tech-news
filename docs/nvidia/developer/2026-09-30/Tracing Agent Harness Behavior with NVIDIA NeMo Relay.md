# Tracing Agent Harness Behavior with NVIDIA NeMo Relay

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-09-30
- **原文連結**: https://developer.nvidia.com/blog/tracing-agent-harness-behavior-with-nvidia-nemo-relay/

## 核心主題
這篇文章介紹如何使用 NVIDIA NeMo Relay 追蹤和檢視 AI Agent 的執行軌跡，透過 ATOF、ATIF 和 OpenTelemetry 三種格式來分析模型調用、工具調用、錯誤重試、延遲和 token 使用情況，並結合任務驗證結果來評估 harness 改進效果。

## 關鍵重點
- **NeMo Relay 提供統一的可觀測層**：整合 Hermes Agent 原生功能，捕捉有序的生命週期事件和有結構的軌跡
- **三種追蹤格式**：ATOF（事件流用於除錯）、ATIF（步驟軌跡用於分析）、OpenTelemetry（跨系統追蹤用於 Phoenix 等工具）
- **兩個實作範例**：簡單終端工具任務（輸出 VALUE=42）和多工具研究任務（搜尋 COLT 2026 會議）
- **Hermes ToolPerf 案例研究**：比較 baseline 和修復版本，Qwen Coder 30B 修復更多任務但增加了調用次數、數據和延遲
- **成功檢查的局限性**：僅確認任務成功無法解釋 Agent 如何從錯誤中恢復或為何需要額外的模型調用

## 結論
透過系統化追蹤和驗證，開發者可以更有效地優化 AI Agent 的執行效率，減少不必要的調用次數和延遲，同時確保任務結果的準確性。

---