# Finish RL Training Faster: Bitwise-Consistent, High-Performance, Agent-Driven

- **來源**: vLLM
- **發布日期**: 2026-10-14
- **原文連結**: https://vllm.ai/blog/2026-10-14-train-inference-consistency

## 核心主題
這篇文章介紹了如何在高性能 RL 訓練中實現訓練與推理的 bitwise 一致性，通過使用相同的推理核進行訓練前向傳播，確保訓練與推理產生完全一致的 logprobs，從而解決訓練不穩定問題。

## 關鍵重點
- 訓練前向直接調用 vLLM 推理核，修改高性能核使其 batch-independent、phase-consistent，確保 rollout 與訓練產生 bitwise 相同的 logprobs（diff = 0）
- 實現四維一致性（kernel determinism、batch independence、phase consistency、cross-GPU consistency）及相同數值合約，並確保 backward 正確
- 開發「train-inference-consistency」技能，包含 11 個檢查門（C0-C10），採用「小模型先解決，再擴展到完整模型」的漸進策略，使用 Agent 自動化定位差異、重現問題並修復
- DeepSeek-V4-Flash：100 步訓練中 91.3% 步驟 diff = 0，達到基線 91.3% 吞吐量；應用到 Nemotron-3.5（Mamba 混合 + NVFP4），SWE-bench Pro 分數維持在 0.6，基線降至 0.22
- 已開源完整工作流程、10 份指南、代碼庫及 Docker 映像，降低新模型實現成本

## 結論
通過實現訓練與推理的 bitwise 一致性，可以顯著提高 RL 訓練的穩定性和效率，減少訓練失敗和重跑，降低實現成本。此方法已驗證於 DeepSeek-V4-Flash 和 Nemotron 模型，並可複製到其他模型上。
---
