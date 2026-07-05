# Run DiffusionGemma on NVIDIA for Developer-Ready, High-Throughput Text Generation

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-10
- **原文連結**: https://developer.nvidia.com/blog/run-diffusiongemma-on-nvidia-for-developer-ready-high-throughput-text-generation/

## 核心主題
NVIDIA 與 Google DeepMind 合作將 DiffusionGemma 最佳化至 NVIDIA 全平台，支援從資料中心 GPU 到桌面工作站的多種部署選項，實現最高每秒 2,000 token 的平行文字生成速度，為開發者提供從原型到生產的低延遲、高吞吐 AI 應用解決方案。

## 關鍵重點
- **多平台性能表現與硬體支援**：DiffusionGemma（26B MoE，激活 3.8B 參數，支援 256K 上下文）在 NVIDIA H100 上達 1,000 tokens/秒、DGX Station 上達 2,000 tokens/秒、DGX Spark 上達 150 tokens/秒；硬體選項涵蓋 DGX Spark（GB10 超級晶片、128GB 統一記憶體、1 PFLOP FP4 計算）、DGX Station（GB300、748GB 相連記憶體、20 PFLOPS FP4 計算）以及桌面 RTX/RTX PRO 系統，並支援 BF16 與 NVFP4 量化格式。
- **Day 0 全面支援生態系**：從 Hugging Face Transformers 初步測試到 vLLM 高吞吐多使用者服務，NVIDIA 提供 Day 0 硬體與軟體整合；開發者可透過 build.nvidia.com 免費試用 GPU 加速端點，使用 NVIDIA Model Optimizer 取得 NVFP4 量化檢查點，並透過 NVIDIA NeMo AutoModel 庫直接在 HuggingFace 檢查點上微調（無需轉換）。
- **NIM 企業級部署與開源承諾**：NVIDIA NIM 以容器化推理微服務形式簡化 DiffusionGemma 從開發到生產的部署，提供標準 OpenAI 相容 API，支援本機、雲端與混合環境運行；NVIDIA 持續貢獻數百個開源專案，並承諾支持 DiffusionGemma 等開源模型以促進 AI 透明度和使用者在 AI 安全與韌性上的協作。

## 結論
NVIDIA 透過 DGX 系列工作站、RTX 桌面系統、vLLM、NIM 與 NeMo AutoModel 等完整工具鏈，讓 DiffusionGemma 的平行擴散文字生成技術從研究原型快速邁向生產部署，為開發者提供涵蓋從本機原型設計到企業級高吞吐服務的全方位解決方案。

---
