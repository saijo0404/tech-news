---
# NVIDIA Accelerates Google DeepMind's DiffusionGemma for Local AI

- **來源**: NVIDIA Blog
- **發布日期**: 2026-06-10
- **原文連結**: https://blogs.nvidia.com/blog/rtx-ai-garage-local-gemma-diffusion/

## 核心主題
NVIDIA 宣布已針對 NVIDIA GeForce RTX 顯示卡、RTX PRO 平台與 DGX Spark 系統最佳化 Google DeepMind 的 DiffusionGemma，讓這款擴散式文字生成模型在本地硬體上實現高達 4 倍的生成速度提升。

## 關鍵重點
- **從記憶體受限轉為運算密集**：傳統自回歸模型逐 token 生成時主要受限於記憶體頻寬，GPU 運算能力大量閒置；DiffusionGemma 每次平行處理 256 個 token，將工作負載轉為運算密集類型，完美發揮 NVIDIA Tensor Cores 的平行運算優勢。
- **多平台高效能部署**：在單一 NVIDIA H100 上達 1,000 tokens/秒、DGX Spark 達 150 tokens/秒、DGX Station 達 2,000 tokens/秒；支援從 GeForce RTX 消費級顯卡、RTX PRO 工作站到 DGX Spark 桌端 AI 超算的完整產品線。
- **開源生態與開發者工具**：以 Apache 2.0 授權提供開放權重，第一天即支援 Hugging Face Transformers、vLLM 與 Unsloth，提供現成的 DGX Spark 與 vLLM 實作指南，並即將支援 llama.cpp，讓開發者能零門檻進行原型開發與微調。

## 結論
NVIDIA 透過硬體與軟體的緊密整合，讓 DiffusionGemma 的擴散式生成架構能在本地環境發揮最大效能，為需要低延遲即時互動的個人使用者與專業工作者提供強大的本地 AI 推論能力，同時降低對雲端服務的依賴與成本。

---
