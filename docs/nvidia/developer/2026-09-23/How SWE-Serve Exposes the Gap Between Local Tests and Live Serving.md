# How SWE-Serve Exposes the Gap Between Local Tests and Live Serving

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-09-23
- **原文連結**: https://developer.nvidia.com/blog/how-swe-serve-exposes-the-gap-between-local-tests-and-live-serving/

## 核心主題
SWE-Serve 是一個評估 AI 編碼代理在推理服務工程任務上表現的新基準，揭示了本地測試與實際服務之間的顯著差距。

## 關鍵重點
- 在包含實際服務測試的 19 個任務中，相同的程式碼片段通過完整驗證器的時間為 45.9%，而排除實際服務測試則為 69.4%，意味著約三分之一通過其他測試的程式碼片段在實際服務測試中失敗。
- 跨越多個運行時領域（如請求處理、排程、模型執行和 KV 快取管理）的任務，其通過率比單一領域任務低 21.3 個百分點，所有測試模型都顯示出相同的差距。
- 評估的 11 個模型中，最佳表現為 Claude Opus 5 和 GPT-5.6 Sol，均為 75% 的 pass@1，但成本和使用時間差異很大，從 $0.95 到 $17.40 不等。

## 結論
SWE-Serve 基準強調了評估推理服務軟件變更時需要檢查完整服務路徑的重要性，包括系統是否通過其公共接口返回正確結果。這表明僅依靠本地測試不足以確保代碼在實際服務環境中的可靠性。

---