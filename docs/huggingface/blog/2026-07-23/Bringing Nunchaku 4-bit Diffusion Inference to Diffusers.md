# Bringing Nunchaku 4-bit Diffusion Inference to Diffusers

- **來源**: Hugging Face
- **發布日期**: 2026-07-23
- **原文連結**: https://huggingface.co/blog/nunchaku-diffusers

## 核心主題
Hugging Face 將 Nunchaku 4-bit 量化推理引擎整合到 Diffusers 框架中，使用戶可以無需額外庫即可載入經過量化的模型，大幅降低 VRAM 使用量並提升推理速度。

## 關鍵重點
- **Nunchaku Lite 簡化載入流程**：用戶只需通過 `from_pretrained()` 即可載入 Nunchaku 量化的模型，無需自訂 pipeline 或本地 CUDA 編譯，CUDA 核函數自動從 Hub 下載。
- **顯著的性能提升**：相比 BF16 基準，Nunchaku Lite 可將峰值 VRAM 降低最多 50%（從 31.1 GB 降至 16-20 GB），推理速度提升約 30%；結合 `torch.compile` 後可達 1.8 倍加速。
- **支援兩種量化方案**：`svdq_w4a4` 用於 transformer 的主要計算（支援 INT4 和 NVFP4），`awq_w4a16` 用於記憶體敏感層（如 FLUX 的適配層），支援 Turing/Ampere/Ada 及 Blackwell GPU。
- **用戶可自定義量化**：通過 `diffuse-compressor` 工具包，用戶可自行量化模型並發布為標準 Diffusers 倉庫，支援 FLUX 等架構。

## 結論
Nunchaku Lite 為 Diffusers 用戶提供了更便捷的 4-bit 量化推理方式，特別適合消費級 GPU 和 Blackwell GPU 用戶，大幅降低門檻並提升性能，是通往高效、低資源消耗的擴增生成模型的重要一步。
---
