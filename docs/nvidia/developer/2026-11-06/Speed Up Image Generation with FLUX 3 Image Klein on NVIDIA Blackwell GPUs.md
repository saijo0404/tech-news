# Speed Up Image Generation with FLUX 3 Image Klein on NVIDIA Blackwell GPUs

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-11-06
- **原文連結**: https://developer.nvidia.com/blog/speed-up-image-generation-with-flux-3-image-klein-on-nvidia-blackwell-gpus/

## 核心主題
本文介紹了 FLUX 3 Image Klein 模型在 NVIDIA Blackwell GPU（B200）上的加速優化方案，通過 TensorRT LLM 實現顯著性能提升。

## 關鍵重點
- **模型架構優化**：結合 Qwen3-VL-4B-Instruct（文字條件）、diffusion transformer（DiT）與 autoencoder，支援 Base 與 distilled 兩個版本
- **單 GPU 加速成效**：單一 B200 GPU 上，結合 PrimsTS + Sol-Attention + Cache-DiT 優化，T2I 快 3.46 倍、I2I 快 4.45 倍
- **多 GPU 擴展**：8 台 B200 GPU 下，T2I 延遲從 14.90s 降至 3.00s（6.01 倍加速），I2I 延遲從 2.73s 降至 1.08s（4.44 倍加速）
- **主要優化技術**：NVFP4 量化（T2I 1.62x）、cuDNN FP8 注意力（1.08x）、VC-Attention FP8（1.18x）、Sol-Attention（1.30x）、Cache-DiT 緩存（1.94x）
- **部署方式**：提供 TensorRT LLM 容器部署指南與 YAML 配置，支援 offline 生成與 online serving

## 結論
NVIDIA 通過 TensorRT LLM 為 FLUX 3 Image Klein 提供了全面的加速優化方案，包括量化、注意力機制優化及多 GPU 擴展，顯著提升生成式模型推論速度，並提供完整的部署指南。

---