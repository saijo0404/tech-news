# NVIDIA Ising Decoding Cuts Color Code Logical Error Rates by Over 300X

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-07-13
- **原文連結**: https://developer.nvidia.com/blog/nvidia-ising-decoding-cuts-color-code-logical-error-rates-by-over-300x/

## 核心主題
NVIDIA 推出 Ising Decoder ColorCode 1 Fast，將 Color Code 量子錯誤糾正解碼器的邏輯錯誤率降低超過 347.7 倍，並提升 7.3 倍運算速度，使 Color Code 重新成為實用選擇。

## 關鍵重點
- Ising Decoder ColorCode 1 Fast 相比現有最佳解碼器 Chromobius，在 d=31 和 0.3% 物理錯誤率下，邏輯錯誤率降低超過 347.7 倍，運行速度快 7.3 倍
- 使用 3D 卷積神經網絡 (CNN) 預解碼器處理三角形 Color Code，支援可擴展、低延遲、高準確性的實時解碼
- NVIDIA 提供完整的開源資源，包括權重、訓練配方、合成數據生成工具 (cuQuantum/cuStabilizer) 和完整訓練管道，讓研究者可針對特定 QPU 架構進行客製化

## 結論
這些成果使 Color Code 重新成為建構和運行真正有用量子電腦的潛在選擇，NVIDIA 提供完整的開源工具和訓練資源供開發者使用。
---