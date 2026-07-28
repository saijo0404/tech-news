# Six Agent Harness Capabilities for Higher Model Performance

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-07-27
- **原文連結**: https://developer.nvidia.com/blog/six-agent-harness-capabilities-for-higher-model-performance/

## 核心主題
NVIDIA 推出的 NOOA 框架透過六項關鍵能力（類型化輸入輸出、引用傳遞、代碼即行動等）提升 AI 代理性能，在軟體工程、資安與推理任務上達到領先表現。

## 關鍵重點
- **物導向設計**：代理是單一 Python 類別，方法即能力、欄位即狀態、文檔字符串即提示、類型註解即強制合約，使代理開發成為傳統軟體開發流程
- **六項核心能力**：類型化輸入輸出、引用傳遞、代碼即行動、可編程循環工程、明確物件狀態、可呼叫 harness API，這些能力直接影響代理性能
- **自訂記憶系統**：代理主動管理記憶，使用 SQLite 儲存，支持知識圖譜，可跨代理共享且保留獨立所有權
- **性能突破**：在 SWE-bench Verified 達 82.2%、CyberGym L1 達 86.8%、ARC-AGI-3 達 85.1%，超越現有最佳表現
- **效率優勢**：使用相同模型但 token 成本降低一半，無需上下文壓縮，相同任務只需 29 次 LLM 調用而非 66 次

## 結論
NOOA 框架證明 harness 設計與模型選擇同等重要，為 AI 代理開發提供可重複、可檢驗、可擴展的開源解決方案，並已公開代碼供社群使用與改進。

---