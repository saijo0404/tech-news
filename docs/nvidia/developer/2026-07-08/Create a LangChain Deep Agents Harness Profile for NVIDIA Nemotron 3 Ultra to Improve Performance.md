# Create a LangChain Deep Agents Harness Profile for NVIDIA Nemotron 3 Ultra to Improve Performance

- **來源**: developer.nvidia.com/blog
- **發布日期**: 2026-07-08
- **原文連結**: https://developer.nvidia.com/blog/create-a-langchain-deep-agents-harness-profile-for-nvidia-nemotron-3-ultra-to-improve-performance/

## 核心主題
這篇文章介紹如何使用 LangChain Deep Agents Harness Profile 技術來優化 NVIDIA Nemotron 3 Ultra 模型的性能，透過 harness engineering 實現無需微調的準確性提升。

## 關鍵重點
- 使用評估基準和 harness profile 修改（如提示修改、中間件插入）來優化 agent，透過迭代評估、分析失敗、提出修改、驗證的循環來優化
- 自動化通過 agentic proposers（如 LangSmith Engine 和 ralph loop）實現自我修正的 harness profile 優化，避免過擬合（overfitting）
- 透過驗證、快照、從失敗中學習、重新檢查整個套件等機制，確保修改有效且不會引入退步

## 結論
透過 harness engineering 技術，可以達到與專有前沿模型相當的準確性，無需微調，使用現有端點即可，為 agent 系統提供了可擴展的優化方法。

---
