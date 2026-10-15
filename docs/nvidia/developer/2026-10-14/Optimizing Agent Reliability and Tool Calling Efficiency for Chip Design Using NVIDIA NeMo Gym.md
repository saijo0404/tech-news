# Optimizing Agent Reliability and Tool Calling Efficiency for Chip Design Using NVIDIA NeMo Gym

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-10-14
- **原文連結**: https://developer.nvidia.com/blog/optimizing-agent-reliability-and-tool-calling-efficiency-for-chip-design-using-nvidia-nemo-gym/

## 核心主題
這篇文章介紹了 NVIDIA NeMo Gym 如何幫助 Siemens EDA 優化 AI 代理在晶片設計工作流程中的可靠性和工具調用效率。

## 關鍵重點
- Siemens Fuse EDA AI Agent 使用 NeMo Gym 評估 Liberty 檔案生成，驗證評分從約 55% 提升至 95%
- 代理操作次數從 155 次減少到 53 次（減少 66%），輸出 token 從 81K 減少到 29K（減少 64%）
- 領域特定驗證器檢查覆蓋率、有效性、相對驗證、準確性和完整性，任何閘失敗即得零分

## 結論
通過最終藝術品評估而非單個工具調用，並使用領域特定驗證器，可以顯著提高工程代理的可靠性。

---