# How to Use AI Agents to Prepare 3D Scenes for Simulation

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-09-16
- **原文連結**: https://developer.nvidia.com/blog/how-to-use-ai-agents-to-prepare-3d-scenes-for-simulation/

## 核心主題
本文介紹如何使用 AI 代理（Codex/Claude 協調，NemoClaw 部署 Hermes 子代理）自動化準備 Blender 3D 場景以進行機器人模擬訓練，使用 NVIDIA Omniverse Libraries 和 OpenUSD 標準。

## 關鍵重點
- **六步驟工作流程**：場景檢查、USD 導出、語義標籤、材質優化、傳感器配置、物理準備
- **三個主要代理**：ovphysx 代理處理物理屬性、ovrtx 代理執行視覺預飛行檢查、SimReady 驗證
- **系統架構**：NemoClaw 協調子代理，Codex/Astra 統籌，Omniverse Libraries 提供工具支援，OpenUSD 作為場景標準
- **應用場景**：將 Blender 場景轉換為 Isaac Sim/Isaac Lab 可使用的模擬場景，解決機器人模擬訓練前的場景準備瓶頸

## 結論
通過 AI 代理工作流，可以自動化重複性的場景準備工作，將 Blender 場景轉換為符合模擬合約的 OpenUSD 世界，從而解決機器人模擬訓練前的場景準備瓶頸。

---