# Accelerating Dropless MoE Training in JAX with NVIDIA Transformer Engine

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-09-14
- **原文連結**: https://developer.nvidia.com/blog/accelerating-dropless-moe-training-in-jax-with-nvidia-transformer-engine/

## 核心主題
NVIDIA Transformer Engine 與 JAX 組合在 Dropless MoE 訓練中實現顯著性能提升，DeepSeek-V3 訓練吞吐量提升約 10 倍。

## 關鍵重點
- **性能提升**：DeepSeek-V3 訓練吞吐量從 103 提升至 1,068 TFLOPS/GPU，達 10.4 倍改善
- **Dropless MoE 優勢**：處理所有 token 無需丟棄或填充，保持模型品質
- **關鍵優化技術**：
  - Grouped GEMM：單一核函數處理變長專家 token 計數
  - NCCL EP：融合 dispatch 與 combine 階段，減少網路流量
  - JAX host offloading：降低記憶體瓶頸
  - XLA multistreaming collectives：並行跨節點通信
- **擴展效率**：在 1,024 GPU 上維持 97% 擴展效率
- **部署方式**：使用 NVIDIA NGC MaxText container（含 Transformer Engine）即可重現

## 結論
此方案已驗證於 NVIDIA GB300 NVL72 硬體，為大規模 MoE 模型訓練提供高效解決方案。

---

本文介紹 NVIDIA 在 DeepSeek-V3 671B 模型訓練上的優化技術，由 NVIDIA AI 平台軟體團隊工程師開發，專注於 Transformer Engine 的 JAX 整合與 MoE 優化。