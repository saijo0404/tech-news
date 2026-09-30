# Getting the Source Right, Not Just the Fact: Source-Aware Verification for MCP Agents

- **來源**: Hugging Face
- **發布日期**: 2026-09-29
- **原文連結**: https://huggingface.co/blog/MultiverseComputingCAI/getting-the-source-right-not-just-the-fact-source

## 核心主題
本文介紹了 ProvenanceGuard 系統，用於多工具 MCP 代理的來源感知事實驗證，解決跨來源混淆問題。

## 關鍵重點
- 傳統來源無視驗證器無法識別事實是否來自正確來源，只檢查事實是否存在於證據池中，導致跨來源混淆問題
- ProvenanceGuard 保留來源身份，將答案分解為具體陳述，檢查每個陳述是否由對應來源支持，並比較來源與答案歸因是否一致
- 在醫療代理測試中，ProvenanceGuard 成功識別出 138/139 個專家認為不應通過的陳述，準確率達 86%，且比傳統驗證器更能精準識別錯誤歸因

## 結論
來源感知驗證對於多工具 MCP 代理至關重要，確保事實不僅正確，而且歸因於正確來源。ProvenanceGuard 作為後生成驗證層，可在不重新訓練代理的情況下，以保守策略保障數據敏感場景中的來源準確性。

---