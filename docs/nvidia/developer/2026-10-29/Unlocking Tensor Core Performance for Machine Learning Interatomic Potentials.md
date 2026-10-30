# Unlocking Tensor Core Performance for Machine Learning Interatomic Potentials

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-10-29
- **原文連結**: https://developer.nvidia.com/blog/unlocking-tensor-core-performance-for-machine-learning-interatomic-potentials/

## 核心主題
本文介紹了如何在 NVIDIA GPU 上使用 Tensor Core 技術（BF16x9 和 TF32x3）來加速機器學習原子間勢能（MLIP）的計算，同時保持與 FP32 相近的精度。

## 關鍵重點
- BF16x9 在 NVIDIA Blackwell GPU 上對 17,280 原子系統的大型 GEMM 加速 2.2–2.5 倍，192 原子系統加速 1.2–1.4 倍，錯誤低於模型自身的非確定性
- TF32x3 在 NVIDIA Ampere GPU 上加速主要 GEMM 1.7–1.9 倍，完整分子動力學步驟加速達 1.5 倍，同時保持力誤差接近 FP32 基準
- TF32x3 在 NVE 軌跡中保持勢能平滑度和能量守恒，與 FP32 行為一致，而單次 TF32 顯示漂移和粗糙
- 在 539 原子 Cantor 合金板片的結構弛豫中，TF32x3 在 218–222 步內收敛，每步加速 1.5 倍，而單次 TF32 即使在 1,000 步後也未達到力容差

## 結論
Tensor Core FP32 方法可以在不重新訓練模型或更改權重架構的情況下，加速 MLIP 推理並保持接近 FP32 基準的行為，為科學機器學習工作載提供新的性能優化途徑。
---
