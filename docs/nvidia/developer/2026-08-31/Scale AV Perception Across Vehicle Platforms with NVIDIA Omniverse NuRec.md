# Scale AV Perception Across Vehicle Platforms with NVIDIA Omniverse NuRec

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-08-31
- **原文連結**: https://developer.nvidia.com/blog/scale-av-perception-across-vehicle-platforms-with-nvidia-omniverse-nurec/

## 核心主題
這篇文章介紹了 NVIDIA Omniverse NuRec 解決方案，用於跨車型自動駕駛感知軟體轉換，通過 3D Gaussian splatting 重建真實駕駛場景並渲染新視角，提供大量神經重建場景用於訓練感知模型。

## 關鍵重點
- 使用 3D Gaussian splatting 重建真實駕駛場景，提供 1,500+ 神經重建場景（每場景約 20 秒，6 路攝影機視角）
- 四步驟工作流程：下載場景、渲染目標視角、優化幀、訓練感知模型
- 測試結果顯示物體檢測精度與召回率相比零射基準有顯著提升
- 數據準備需要三個 Parquet 文件（位置、軌跡、感知數據），所有視頻需同步且覆蓋相同記錄時間段
- 使用 NCore V4 格式轉換數據，包含相機影像、內參、外參、姿態、掩蓋和物體軌跡等組件
- 輔助數據生成包括分割掩碼、深度圖、自車掩蓋和元數據
- 需要 NVIDIA NGC 或 Hugging Face 帳戶及授權

## 結論
NuRec 解決方案通過合成數據有效解決了自動駕駛感知軟體轉換到新車型時數據成本高昂的問題，提供了一套完整的自動化工作流程，可大幅降低收集新車型真實數據的成本。
---