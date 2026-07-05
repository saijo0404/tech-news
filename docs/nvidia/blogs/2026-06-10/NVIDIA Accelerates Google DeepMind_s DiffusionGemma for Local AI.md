# NVIDIA Accelerates Google DeepMind's DiffusionGemma for Local AI

- **來源**: NVIDIA Blogs
- **發布日期**: 2026-06-10
- **原文連結**: https://blogs.nvidia.com/blog/rtx-ai-garage-local-gemma-diffusion/

## 核心主題
NVIDIA 將 Google DeepMind 發布的 DiffusionGemma 最佳化至 NVIDIA GeForce RTX 顯示卡、RTX PRO 平台與 DGX Spark 系統，實現從本地 PC 到雲端的高效平行文字生成，單用戶場景下速度達自回歸模型的 4 倍。

## 關鍵重點
- **平行生成打破記憶體頻寬瓶頸**：DiffusionGemma 不逐字生成而是以擴散去噪方式每步平行處理最多 256 個 token，將原本記憶體驗配瓶頸的序列問題轉為計算密集型工作負載——正符合 NVIDIA Tensor Cores 的強項；在 H100 上達 1,000 tokens/秒、DGX Station 達 2,000 tokens/秒、DGX Spark 達 150 tokens/秒。
- **多層級硬體部署選項**：從本地到雲端全面支援——DGX Spark（GB10 超級晶片、128GB 統一記憶體，預裝 NVIDIA AI 軟體堆疊）、RTX PRO 6000 工作站（專業開發者低延遲生成與代理迴圈）、DGX Station（GB300、748GB 相連記憶體，最高 2,000 tokens/秒）、以及 GeForce RTX 顯示卡（llama.cpp 支援即將推出）；所有平台支援 BF16 與 NVFP4 量化。
- **Day Zero 開源生態系整合**：模型以 Apache 2.0 授權開放權重，零日支援 Hugging Face Transformers（RTX 5090/DGX Spark 可直接執行）、vLLM（高吞吐服務）、Unsloth 與 NVIDIA NeMo Framework（微調）；開發者可透過 Hugging Face 免費測試或使用 build.nvidia.com 的 NVIDIA 託管 API 試用。

## 結論
NVIDIA 以 RTX AI Garage 的深度硬體優化，將 DiffusionGemma 的擴散式平行生成技術從研究原型推至本地 AI 開發者、研究人員與 AI 愛好者的桌面，讓單用戶、低延遲的互動式 AI 工作流不再受傳統自回歸模型的速度限制。

---
