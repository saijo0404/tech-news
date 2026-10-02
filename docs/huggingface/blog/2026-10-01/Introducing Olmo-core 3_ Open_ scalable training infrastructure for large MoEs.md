# Introducing Olmo-core 3: Open, scalable training infrastructure for large MoEs

- **來源**: Hugging Face
- **發布日期**: 2026-10-01
- **原文連結**: https://huggingface.co/blog/allenai/olmocore3

## 核心主題
Olmo-core 3 是 Hugging Face 推出的全新開源混合專家（MoE）訓練框架，旨在將大語言模型的訓練規模擴展至兆參數級別，同時保持計算效率。

## 關鍵重點
- **架構升級**：從完全分片數據並行（FSDP）改為分佈式數據並行（DDP），專家參數從 4.6B 提升至 47B，每 token 活躍參數保持約 3.2B，訓練吞吐量提升 2.7 倍
- **優化技術**：採用專家並行、流水線並行、分佈式優化器、行式專家並行、GPU 駐留路由、分組 GEMM 等技術，並支援 MXFP8 低精度格式，訓練吞吐量提升 21%
- **兆參數訓練**：已在 NVIDIA B300 GPU 上測試，最高支援 1.2 兆參數模型（512 GPU），最高吞吐量達 858 TFLOP/s/GPU，甚至實驗性達到 2.38 兆參數
- **完全開源**：提供技術報告、GitHub 代碼和互動演示，讓研究者可自由使用、修改和擴展

## 結論
Olmo-core 3 是下一代 Olmo 模型的基礎，完全開源，讓研究者和開發者能自由訓練和實驗，推動大模型訓練基礎設施的開放發展。
---
