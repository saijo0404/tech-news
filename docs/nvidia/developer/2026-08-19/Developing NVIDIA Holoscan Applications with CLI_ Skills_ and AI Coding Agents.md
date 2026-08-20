# Developing NVIDIA Holoscan Applications with CLI, Skills, and AI Coding Agents

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-08-19
- **原文連結**: https://developer.nvidia.com/blog/developing-nvidia-holoscan-applications-with-cli-skills-and-ai-coding-agents/

## 核心主題
本文介紹了如何使用 NVIDIA Holoscan、HoloHub 和 AI 編碼代理，通過迭代開發方式構建實時內窺鏡工具分割應用。

## 關鍵重點
- **迭代開發流程**：工程師定義目標與限制，AI 代理使用 Holoscan CLI 和 HoloHub 文檔實現功能，然後進行基準測試與優化
- **三次迭代優化**：從建立最小可運行應用（Iteration 1）到實施基準測試（Iteration 2），再到降低延遲（Iteration 3）
- **性能優化成果**：渲染吞吐量提高 50.5%（204.0 FPS → 306.9 FPS），應用路徑延遲降低 33.6%（4.891 ms → 3.247 ms）
- **最佳開發工作流**：消融研究證明，同時提供 CLI、技能和文檔/示例時，開發效率最高（40 分鐘，11M tokens），優於單獨使用文檔（65 分鐘，20M tokens）或 CLI（40 分鐘，15M tokens）

## 結論
本文展示了 AI 代理如何與工程師協同，利用 Holoscan CLI、開發技能和文檔示例，通過迭代方式高效開發實時 AI 應用。最佳實踐是結合 CLI、技能和文檔/示例的完整資源組合，可獲得最高品質的開發工作流和最低資源開銷。

---