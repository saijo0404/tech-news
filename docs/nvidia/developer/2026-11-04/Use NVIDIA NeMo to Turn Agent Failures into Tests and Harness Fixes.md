# Use NVIDIA NeMo to Turn Agent Failures into Tests and Harness Fixes

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-11-04
- **原文連結**: https://developer.nvidia.com/blog/use-nvidia-nemo-to-turn-agent-failures-into-tests-and-harness-fixes/

## 核心主題
這篇文章介紹了如何使用 NVIDIA NeMo 工具套件（包括 NeMo Compass、NeMo Eval Author 和 NeMo Relay）建立完整的代理優化循環，將代理失敗轉化為測試並利用測試結果進行修復。

## 關鍵重點
- **NeMo Compass**：分析儲存的代理追蹤記錄，識別重複問題、優先級排序改進項目，並將每個發現與特定追蹤 ID 連結
- **NeMo Eval Author**：提供編碼代理技能和工作流程，協助在 Harbor 或 NVIDIA NeMo Gym 格式中建立自訂評估，測量代理行為是否符合領域需求
- **優化循環**：完整的優化循環包括更新代理 harness（如修改 Hermes SOUL.md 系統提示），然後在開發和保留任務上重新執行評估以驗證改進並檢測退步
- **實際案例**：在達索系統工程案例中，同一循環將錯誤的工具有效呼叫從 142 次減少到零，並在六個場景中實現 28% 的相對評估分數提升，每輪減少 35% 的工具有效呼叫

## 結論
通過建立「追蹤記錄→評估測試→harness 更新→重新評估」的優化循環，NVIDIA NeMo 工具套件能夠系統化地識別和修復代理問題，不僅提升任務質量，還提高執行效率，為生產環境中的代理優化提供可重複的框架。
---