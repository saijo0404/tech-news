# How to Use NVIDIA Warp and MjWarp to Accelerate Robotics Simulation and Learning Workflows

- **來源**: Hugging Face Blog
- **發布日期**: 2026-09-23
- **原文連結**: https://huggingface.co/blog/nvidia/how-to-use-nvidia-warp-and-mjwarp

## 核心主題
本文介紹 NVIDIA Warp 與 MJWarp 技術，用於 GPU 加速的 MuJoCo 物理模擬，提升機器人模擬與學習工作流的效率。

## 關鍵重點
- **NVIDIA Warp**：Python 框架，用於撰寫高性能 GPU 加速核，支援靜態類型編譯
- **MJWarp**：NVIDIA Warp 的 MuJoCo 物理實現，將模擬移至 GPU 加速，適合大規模並行模擬（如 RL 訓練）
- **性能優化技巧**：CUDA graph capture（一次捕捉，多次重播）、緊密調整記憶體參數 (nconmax/naconmax/njmax)、使用 mjwarp-testspeed 測試記憶體分配
- **批量擴展**：從單世界擴展至 2,048 世界，透過 np.tile 複製初始狀態，利用 CUDA Graphs 優化執行效率
- **工具鏈**：提供 warp-lang、mujoco-warp 安裝指引，並連結 GitHub 與 Colab 教學

## 結論
透過使用 NVIDIA Warp 和 MJWarp，可以大幅提升機器人模擬與學習工作流的效率，特別適合 RL 訓練等需要大量並行環境的場景。建議先建立 MuJoCo CPU 基準，驗證堆疊成功條件後再遷移至 MJWarp。

---