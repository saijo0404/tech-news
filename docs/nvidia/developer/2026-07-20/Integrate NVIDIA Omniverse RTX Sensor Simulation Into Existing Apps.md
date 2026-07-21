# Integrate NVIDIA Omniverse RTX Sensor Simulation Into Existing Apps

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-07-20
- **原文連結**: https://developer.nvidia.com/blog/integrate-nvidia-omniverse-rtx-sensor-simulation-into-existing-apps/

## 核心主題
這篇文章介紹了 NVIDIA Omniverse RTX 感測器模擬 (ovrtx) 如何整合到現有應用程式中，提供模組化 API 支援攝影機、LiDAR、雷達等感測器模擬。

## 關鍵重點
- ovrtx 提供輕量級 C/Python SDK，可整合至現有應用程式（CAD、Blender、機器人、雲端設計工作流）
- 支援 OpenUSD 場景，可自定義感測器輸出（攝影機、LiDAR、雷達、深度、法線、語義分割等）
- 可透過 CPU/GPU 記憶體輸出，使用 DLPack、NumPy 或 PyTorch
- 提供最小化示例、瀏覽器串流視圖、物理模擬整合等應用範例
- 可透過 NVIDIA Omniverse GitHub Repo 獲取工具，本地部署可在 NVIDIA DGX Station 使用 NemoClaw 完成

## 結論
ovrtx 作為預發布軟體，為開發者提供了模組化、易於整合的 RTX 感測器模擬解決方案，可大幅提升現有應用程式的渲染與模擬能力。
---