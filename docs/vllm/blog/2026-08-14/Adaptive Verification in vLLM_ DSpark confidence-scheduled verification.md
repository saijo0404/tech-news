# Adaptive Verification in vLLM: DSpark confidence-scheduled verification

- **來源**: vLLM Blog
- **發布日期**: 2026-08-14
- **原文連結**: https://vllm.ai/blog/2026-08-14-dspark-adaptive-verification

## 核心主題
vLLM 引入了 DSpark 的適應性驗證功能，根據每個 draft token 的置信度動態決定驗證範圍，而非固定驗證長度，從而優化了不同並發場景下的推論性能。

## 關鍵重點
- DSpark 通過置信度頭（confidence head）為每個 draft token 評分，根據生存機率動態分配驗證預算，取代了固定驗證長度的方式
- 適應性驗證在並發度 1 到 256 的範圍內都能保持性能優勢，無需手動調整 num_speculative_tokens 參數
- 實現了變長 decode CUDA graphs 以支持不同大小的驗證批次，並使用成本模型優化驗證策略
- 在 DeepSeek-V4-Pro-0813 模型上測試，適應性驗證在整個並發度範圍內都位於帕累托前沿，表現優於固定驗證策略

## 結論
這項技術使 DSpark 成為更易於上線的解決方案，能夠自動適應不同工作負載，無需用戶手動調參即可在各種並發場景下獲得最佳性能。
---
