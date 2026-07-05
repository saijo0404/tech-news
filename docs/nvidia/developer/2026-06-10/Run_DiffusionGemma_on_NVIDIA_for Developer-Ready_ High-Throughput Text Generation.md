# Run DiffusionGemma on NVIDIA for Developer-Ready, High-Throughput Text Generation

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-10
- **原文連結**: https://developer.nvidia.com/blog/run-diffusiongemma-on-nvidia-for-developer-ready-high-throughput-text-generation/

## 核心主題
NVIDIA 宣布 Google DeepMind 的 DiffusionGemma 已在 NVIDIA 平台完成最佳化，開發者可以透過 DGX、RTX 等硬體與 vLLM、NIM、NeMo 等工具鏈，高效部署這款每秒可生成上千 token 的擴散式文字生成模型。

## 關鍵重點
- **極高吞吐量與多平台支援**：DiffusionGemma 每次前向傳播平行生成 256 個 token，在單一 NVIDIA H100 上可達 1,000 tokens/秒、DGX Station 達 2,000 tokens/秒；支援從 DGX Spark（桌端 AI 超算）、DGX Station 到 RTX / RTX PRO 等各式平台，量化後亦可在 GeForce RTX 5090 等消費級顯卡上運行。
- **Day 0 完整開發支援**：提供 Hugging Face Transformers 快速原型、vLLM 高併發推論、NIM 容器化企業部署（OpenAI 相容 API），以及 NeMo AutoModel 微調工具，讓開發者從實驗到生產一氣呵成。模型同時支援 BF16 與 NVFP4 4-bit 精確度。
- **模型規格與開源承諾**：DiffusionGemma 採用 Gemma 4 26B A4B MoE 架構，總參數 25.2B、推理僅激活 3.8B，支援最高 256K token 上下文長度；NVIDIA 強調對開源模型與生態系的投入，促進 AI 透明度和安全性。

## 結論
NVIDIA 透過從硬體到軟體的全方位支援，讓 DiffusionGemma 能從原型快速推進到生產環境，為需要低延遲、高併發即時 AI 應用的開發者提供高效能的文字生成解決方案。

---
