# Efficient MoE Training for Biological Foundation Models

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-09-24
- **原文連結**: https://developer.nvidia.com/blog/efficient-moe-training-for-biological-foundation-models/

## 核心主題
這篇文章介紹了 NVIDIA Transformer Engine 如何優化混合專家(MoE)架構的生物基礎模型訓練，通過分組線性運算、MXFP8 精度和融合核函數來提升訓練效率。

## 關鍵重點
- **GroupedLinear 優化專家計算**：將多個專家線性運算合併為單一分組操作，大幅減少 GPU 啟動過載和調度開銷
- **MXFP8 8-bit 精度訓練**：相比 BF16 減少記憶體使用量，在 NVIDIA Blackwell GPU 上可硬體加速
- **融合核函數技術**：將 GroupedLinear、ScaledSwiGLU 和路由權重縮放融合為單一 ForwardGroupedMLP_CuTeGEMMSwiGLU_MXFP8 核函數
- **BioNeMo 配方效能提升**：在八張 NVIDIA B200 Tensor Core GPU 上訓練，比 Hugging Face 基線快達 2.21 倍

## 結論
NVIDIA Transformer Engine 提供的優化技術為訓練 MoE 生物基礎模型提供了實用的參考，特別適合處理大參數量和長序列的基因組工作負載。

---