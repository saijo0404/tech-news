# Experiment with Qwen3.8-Flash-Next 176B Model on NVIDIA GB300 NVL72 for Agentic Coding

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-08-26
- **原文連結**: https://developer.nvidia.com/blog/experiment-with-qwen3-8-flash-next-176b-model-on-nvidia-gb300-nvl72-for-agentic-coding/

## 核心主題
Alibaba 推出 Qwen3.8-Flash-Next 大語言模型，並由 NVIDIA 驗證可在 GB300 NVL72 上運行，專為代理編程等長上下文應用設計。

## 關鍵重點
- **模型架構創新**：採用 Gated DeltaNet (GDN) 和 Qwen 稀疏注意力 (QSA) 混合架構，支援 100 萬 token 上下文，透過 GDN 壓縮歷史上下文並使用 QSA 進行精確檢索
- **性能提升**：QSA 架構在 100 萬 token 工作負載上，prefill 速度提升 7.6 倍，decoding 速度提升 4.9 倍，在 90% 前綴快取命中率下達到 8.6 倍 prefilled throughput
- **硬體支援**：可在 NVIDIA GB300 NVL72（整合 72 張 Blackwell Ultra GPU）上運行，每秒處理超過 16K tokens，也支援本地 NVIDIA 硬體如 DGX Station、DGX Spark 集群和 RTX PRO 6000 Blackwell 工作站
- **開發者工具**：支援 NVIDIA NeMo AutoModel 微調（全量 SFT 或 LoRA）、NeMo RL 強化學習，以及 SGLang、vLLM、TokenSpeed 等多種推理引擎

## 結論
此模型為開發者提供了實驗和評估下一代 Qwen4 架構的機會，可從 QwenCloud 試用或從 Hugging Face/ModelScope 下載權重進行本地開發和評估。

---