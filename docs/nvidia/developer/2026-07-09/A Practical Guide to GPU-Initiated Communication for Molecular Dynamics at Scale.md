# A Practical Guide to GPU-Initiated Communication for Molecular Dynamics at Scale

- **來源**: developer.nvidia.com/blog
- **發布日期**: 2026-07-09
- **原文連結**: https://developer.nvidia.com/blog/a-practical-guide-to-gpu-initiated-communication-for-molecular-dynamics-at-scale/

## 核心主題
這篇文章介紹了如何使用 NVIDIA NVSHMEM 技術實現 GPU 啟動的遠端記憶體存取，解決 GROMACS 分子動力學模擬中傳統 MPI 通訊的 CPU-GPU 同步瓶頸問題。

## 關鍵重點
- 傳統 GROMACS 使用 CPU 協調的 MPI 通訊，每個時間步需 12 次阻塞式同步，嚴重限制現代異質集群的迭代速率
- 引入 NVIDIA NVSHMEM 實現 GPU 啟動的遠端記憶體存取，在融合核內完成裝置端打包、傳輸和信號，消除 CPU 從通訊關鍵路徑
- 採用依賴感知的核融合技術，將每個脈衝的原子索引圖分為獨立和依賴子集，將每個時間步的核啟動從 6 個減少至 1 個，利用 NVLink 直接存儲和 RDMA 網絡傳輸優化傳輸路徑

## 結論
透過 GPU 啟動的通訊優化技術，在 NVIDIA Eos 超級計算機和 NVIDIA GB200 NVL72 集群上實現了 1.3-2 倍的強縮放性能提升，為任何具有邊界交換模式的 HPC 應用提供了可擴展的解決方案。

---
