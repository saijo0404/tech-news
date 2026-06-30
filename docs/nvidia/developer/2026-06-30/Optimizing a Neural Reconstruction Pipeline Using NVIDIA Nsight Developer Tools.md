---
# Optimizing a Neural Reconstruction Pipeline Using NVIDIA Nsight Developer Tools

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-30
- **原文連結**: https://developer.nvidia.com/blog/optimizing-a-neural-reconstruction-pipeline-using-nvidia-nsight-developer-tools/

## 核心主題
NVIDIA 工程師分享如何使用 Nsight Systems 和 Nsight Compute 工具優化 NuRec（神經重建管線）的 GPU 效能，將關鍵函式加速近 50 倍，並透過分離運算與移除同步點大幅提升 GPU 利用率。

## 關鍵重點
- **Nsight Systems 發現 GPU 嚴重闲置**：初始假設渲染核心佔用最多時間，但 Nsight Systems 的 CUDA HW 時間軸顯示 GPU 大部分時間未充分利用。深入分析後發現 `collect_gaussian_parameters`（特別是 `interpolate` 函式，佔 4.184 ms）因呼叫大量小核心和記憶體操作拖慢進度；透過將多個小核心融合為單一核心，該函式從 4.184 ms 縮短至 **83.81 μs（近 50 倍加速）**。此外，移除冗長的 `cudaStreamSynchronize` 同步點，讓 CPU 能無縫排隊工作，GPU 利用率從斷斷續續變成緊湊滿載。
- **Nsight Compute 優化 renderBackward 核心**：此核心同時處理相機和激光雷達（lidar）資料，但兩者行為和資源需求差異巨大，卻都靜態分配 167 個暫存器和相同共享記憶體，導致 occupancy 僅約 15%。團隊將核心拆分為相機版和 lidar 版，分別調整 `launch_bounds` 和共享記憶體配置，並使用 `cudaFuncSetCacheConfig` 偏好更大共享記憶體。優化後，lidar 和相機核心的暫存器分配分別降至 64 和 128，共享記憶體減半，occupancy 從 15% 提升至 **30-50%**，最長的 lidar 核心從 31 ms 降至 18 ms。
- **目標：即時重建**：NuRec 用於從多感測器資料（相機、激光雷達）重建高保真 3D 環境，供自主駕駛和機器人平台的模擬使用。初始重建短片段需 1 小時以上，長期目標是實現 **即時重建**（30 秒片段 30 秒內完成）。除了重建速度，渲染階段的大量框架生成（用於強化學習和合成數據）也因效能提升而顯著降低 GPU 時間與基礎設施成本。

## 結論
這是一篇典型的 GPU 效能優化案例：先用 Nsight Systems 從系統層面找出瓶頸（小核心過多、同步點阻塞），再用 Nsight Compute 深入核心層面調整資源配置（分離不同輸入類型、動態調整暫存器和共享記憶體）。透過這兩款免費工具的協同使用，團隊成功將 NuRec 重建管線的效能推向「即時」目標，為神經重建和物理 AI 的開發效率帶來重大提升。

---
