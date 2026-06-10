# 在 NVIDIA GPU 上運行 Step 3.7 Flash，邁向企業級多模態 AI

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-05-29
- **原文連結**: https://developer.nvidia.com/blog/run-step-3-7-flash-on-nvidia-gpus-with-enterprise-ready-multimodal-ai/

## 核心主題
StepFun 推出 198B 參數的 Step 3.7 Flash 視覺語言模型，NVIDIA 提供完整工具鏈讓開發者在 GPU 上進行原型測試、生產部署與微調，實現企業級多模態 AI 應用。

## 關鍵重點
- **198B MoE 模型，高效能多模態推理**：Step 3.7 Flash 採用混合專家架構，擁有 288 個專家（每次前向傳播僅激活 8 個，約 11B 參數），支援 256K 上下文視窗、三種可配置的推理等級，以及原生圖片與影片輸入，適合財務分析、程式碼代理等高吞吐量場景。
- **NIM 生產級部署與 NEMO 微調**：NVIDIA NIM 提供容器化推理微服務，支援 OpenAI 相容 API，可於本地、雲端或混合環境一鍵部署；NVIDIA NeMo Automodel 則提供 Day 0 微調能力，在 Hopper GPU 上以 600 tokens/sec 執行 LoRA 微調，無需檢查點轉換。
- **靈活部署選項**：從資料中心的 Blackwell 叢集到桌邊的 DGX Station（748 GB 一致記憶體，足以容納完整 256K 上下文），搭配 SGLang、TensorRT-LLM、vLLM 等開源框架與 NVFP4 量化權重，開發者可依需求選擇最佳方案。

## 結論
NVIDIA 透過 NIM、NEMO Framework 與多硬體選項，為 Step 3.7 Flash 打造了從原型到生產的完整路徑，讓企業能快速部署高效能多模態 AI 應用，同時保持對開源生態的承諾。
