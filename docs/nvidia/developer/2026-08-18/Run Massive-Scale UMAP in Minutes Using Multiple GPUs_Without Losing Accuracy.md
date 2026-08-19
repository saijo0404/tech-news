# Run Massive-Scale UMAP in Minutes Using Multiple GPUs—Without Losing Accuracy

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-08-18
- **原文連結**: https://developer.nvidia.com/blog/run-massive-scale-umap-in-minutes-using-multiple-gpus-without-losing-accuracy/

## 核心主題
NVIDIA cuML 和 cuVS 推出了多 GPU 支援的 UMAP 實現，可大幅加速大規模數據集處理，同時保持嵌入品質。

## 關鍵重點
- 通過將數據集分組並獨立計算局部 kNN 圖，實現了端到端的分佈式計算，避免了昂貴的「全對全」通信。
- 在 MIRACL 和 Wiki 數據集上測試，使用八張 NVIDIA H100 GPU 可達 74 倍加速，使數百 GB 的數據集處理變得可行。
- 通過調整 `knn_n_clusters` 和 `knn_overlap_factor` 參數，可在空間、時間和品質之間取得可控制的權衡。

## 結論
這項技術使 UMAP 能夠在幾分鐘內完成原本需要數小時甚至數天的任務，讓大規模數據降維變得更加實用和高效。

---