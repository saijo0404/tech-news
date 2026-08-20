# Evaluating AI Agent Skill Performance with NVIDIA SkillEvaluator

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-08-19
- **原文連結**: https://developer.nvidia.com/blog/evaluating-ai-agent-skill-performance-with-nvidia-skillevaluator/

## 核心主題
NVIDIA 推出 SkillEvaluator 工具，透過三層評估流程（靜態檢查、獨特性分析、實測任務）來衡量驗證技能對 AI 代理的性能影響，測試超過 300 個技能在 30+ 產品上的表現。

## 關鍵重點
- 驗證技能在正確性、可發現性、有效性和效率四個維度上平均提升 31 分（不含安全性則為 39 分）
- 產品領域和評估設計對技能提升的影響大於代理工具選擇
- 部分技能可顯著減少 token 使用（如 jetson-optimize-memory 減少 76.9%），但有些技能反而增加 token 使用

## 結論
SkillEvaluator 提供了客觀的評估框架，幫助開發者更精準地優化技能，但需要針對特定場景進行優化，因為 token 節省並非自動發生。
---
