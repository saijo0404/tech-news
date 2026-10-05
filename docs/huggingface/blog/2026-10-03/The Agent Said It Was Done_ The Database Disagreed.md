# ThinkingBox 評測框架

- **來源**: Hugging Face Blog
- **發布日期**: 2026-10-03
- **原文連結**: https://huggingface.co/blog/microsoft/thinkingbox

## 核心主題
Microsoft 與 Hugging Face 合作推出 ThinkingBox 評測框架，不再以 AI Agent 生成的句子為評量標準，而是根據其留下的紀錄與副作用來評分。

## 關鍵重點
- **單一成功≠可靠**：在 507 個業務工作流中，79,853 次嘗試有 79.85% 失敗，即使終止乾淨仍有 77.61% 存在錯誤欄位值
- **三個關鍵指標**：pass@1（單一嘗試成功率）、pass@20（20 次嘗試中至少一次成功）、Observed 20/20（所有 20 次嘗試都成功）
- **成本分析**：GPT-5.6 Sol 每成功任務成本最低 ($0.127)，GPT-5.4 每可靠任務成本最便宜 ($6.80)，但僅 128 任務達標
- **失敗模式**：79.9% 失敗來自工具處理問題，建議檢查終端狀態、分類錯誤以便重試、縮減工具表面、要求人工批准不可逆變更
- **ThinkingBox-Bench**：提供二進位通過/失敗獎勵機制，專注於失敗分析與重現性測試
- **OpenEnv 環境**：支援真實記錄評估，需要 Linux/WSL、Python 3.11+、uv、Docker、ThinkingBox CLI 等組件
- **授權資訊**：ThinkingBox 代碼 MIT 授權、Benchmark 數據 CDLA-Permissive-2.0、OpenEnv 環境 BSD-3-Clause

## 結論
ThinkingBox 評測框架透過關注實際執行紀錄而非單一成功，更真實地反映 AI Agent 的可靠性。使用者應重視 pass@20 與 Observed 20/20 指標，並針對工具處理問題優化工作流設計。

---