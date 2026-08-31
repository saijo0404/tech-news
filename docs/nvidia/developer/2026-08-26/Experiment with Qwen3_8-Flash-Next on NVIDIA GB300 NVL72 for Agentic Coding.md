# Experiment with Qwen3.8-Flash-Next on NVIDIA GB300 NVL72 for Agentic Coding

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-08-26
- **原文連結**: https://developer.nvidia.com/blog/experiment-with-qwen3-8-flash-next-on-nvidia-gb300-nvl72-for-agentic-coding/

## 核心主題
Alibaba 推出 Qwen3.8-Flash-Next 多模態混合專家模型，並驗證其在 NVIDIA GB300 NVL72 架構上的高性能表現，專為代理編碼等長上下文應用設計。

## 關鍵重點
- **模型架構創新**：結合 Gated DeltaNet (GDN) 與 Qwen 稀疏注意力 (QSA)，將 125B 參數模型壓縮至每 token 僅激活 6B 參數，原生支持 262,144-token 上下文並可擴展至 1M tokens。
- **性能突破**：在 1M-token 工作負載下，QSA 架構相比全注意力機制提供最高 7.6 倍預填充速度和 4.9 倍解碼速度提升，prefill 吞吐量達 Qwen3.7-Plus 的 8.6 倍。
- **NVIDIA GB300 NVL72 部署**：在整合 72 張 Blackwell Ultra GPU 的 GB300 NVL72 平台上，實現每 GPU 超過 16K tokens/秒的吞吐量，支持高併發、低延遲的代理編碼應用。
- **開發者工具鏈**：提供 NVIDIA NeMo AutoModel 微調、NeMo RL 強化學習，以及 SGLang、vLLM、TokenSpeed 等多種推理引擎支援。

## 結論
Qwen3.8-Flash-Next 展示了 NVIDIA 與 Alibaba 合作在長上下文 AI 模型上的最新進展，透過混合架構與 Blackwell 硬體組合，為開發者提供從原型到生產環境的完整解決方案。建議立即透過 QwenCloud 測試模型或從 Hugging Face 下載權重進行本地開發。

---