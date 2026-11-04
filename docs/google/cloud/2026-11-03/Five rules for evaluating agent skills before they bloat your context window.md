# Five rules for evaluating agent skills before they bloat your context window

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-04
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/evaluate-agent-skills-before-they-bloat-your-context-window/

## 核心主題
這篇文章提出了五項工程規則，用於在將 AI 技能（SKILL.md）加入代碼代理之前進行評估，以避免無效地膨脹上下文窗口。

## 關鍵重點
- **檢查觸發衝突與安全風險**：在啟動容器前，應先驗證 YAML 前導面的觸發條件，避免技能未被載入或與其他技能衝突。推薦使用 skill-reach 工具進行碰撞檢測。
- **避免在開發者筆記本上運行評估**：開發環境存在變數、權限和資源干擾，會導致評估結果失真。應在隔離的沙盒環境中進行測試。
- **採用配對的 WITH vs. W/OUT 消融測試**：單次測試不可靠，應通過多次重複運行（Pass@3）比較加入技能與未加入技能的差異，才能真實反映技能價值。
- **將效率、安全與正確性分開評估**：防止代理「獎勵黑客」行為，需確保評估維度獨立，並加入安全檢查（如禁止讀取敏感憑證）。
- **編碼操作習慣而非文檔轉錄**：技能應教導具體的操作習慣（如驗證 CLI 參數、按需路由、最小權限認證），而非複製冗長的 API 文檔。

## 結論
透過嚴格遵循這五項規則，開發者可以確保 AI 技能真正提升代理表現，同時避免無效消耗上下文窗口和資源。刪除不再必要的技能也是優化團隊的重要一步。

---