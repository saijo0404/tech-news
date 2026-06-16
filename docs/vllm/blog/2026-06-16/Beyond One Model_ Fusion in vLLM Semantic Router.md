---
# Beyond One Model: Fusion in vLLM Semantic Router

- **來源**: vLLM Blog
- **發布日期**: 2026-06-16
- **原文連結**: https://vllm.ai/blog/2026-06-16-vllm-sr-fusion-api

## 核心主題
vLLM Semantic Router（vLLM-SR）推出 Fusion 新功能，將「多模型面板 + 評判者 + 綜合」模式納入路由原語，讓系統能根據請求特徵自動決定是否啟用多模型協作，而非僅依賴單一模型服務。

## 關鍵重點
- **Fusion 工作流程：面板、評判、綜合**：Fusion 讓路由策略能同時呼叫多個獨立模型（面板）產生候選答案，再由評判模型分析共識、矛盾、部分覆蓋、獨特洞察與盲點，最後綜合為單一使用者回應。此流程可追蹤哪些模型參與、執行次數、失敗記錄與總 Token 用量，提供完整的可觀測性。
- **三種進入方式與策略驅動**：（1）`vllm-sr/auto` 讓路由器自動判斷請求是否需要 Fusion，簡單請求走單模型快路線；（2）`vllm-sr/fusion` 明確指定僅使用 Fusion 路由，若不匹配則回報錯誤而非靜態退回單模型；（3）Request Plugin 允許單一請求覆寫面板配置。所有面板、評判者、錯誤處理與併發限制（max_concurrent、on_error）均由路由決策級配置，而非全域設定。
- **OpenRouter DRACO 結果驗證多模型優勢**：OpenRouter 在 DRACO 深層研究基準測試中顯示，Fusion 面板（如 Fable 5 + GPT-5.5）以 69.0% 分數顯著超越單模型 Claude Fable 5（65.3%）與 DeepSeek V4 Pro（60.3%），證明獨立模型多樣性能復原單一較便宜模型所缺乏的品質——這正是路由器應該控制的 tradeoff。

## 結論
Fusion 不該是預設行為，而該是路由決策。vLLM-SR 將模型品質視為「不僅取決於檢查點，更取決於圍繞該檢查點的服務系統」，讓營運者能精確控制何時值得為額外地延遲付出代價。隨著 AI 應用日益複雜，最佳答案將不再來自單一最大的模型，而是來自最佳的模型系統——而 vLLM-SR 正是讓此系統可程式化的基礎設施。

---
