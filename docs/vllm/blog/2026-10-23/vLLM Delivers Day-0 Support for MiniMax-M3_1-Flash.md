# vLLM Delivers Day-0 Support for MiniMax-M3.1-Flash

- **來源**: vLLM Blog
- **發布日期**: 2026-10-23
- **原文連結**: https://vllm.ai/blog/2026-10-23-minimax-m31-flash

## 核心主題
vLLM 提供對 MiniMax-M3.1-Flash 模型的 Day-0 支援，支援 NVIDIA Blackwell、Rubin 和 AMD MI350 系列 GPU，並帶來顯著的性能優化。

## 關鍵重點
- **MiniMax 稀疏注意力 (MSA) 架構**：採用 NVFP4 KV Cache 和 NVFP4 MoE 權重，大幅降低記憶體使用，Checkpoint 體積減少 44.6%，每 token 節省 43.75% 記憶體
- **NVIDIA Blackwell 專用優化**：利用 CUDA 13.4 QMUL4 指令，索引 QK 解碼最快達 1.7 倍，稀疏注意力解碼最快達 1.3 倍
- **NVIDIA Rubin 專用優化**：針對 SM107 架構優化，利用更大共享記憶體和更多 SM 數量，性能進一步提升
- **AMD MI350 系列支援**：提供 NVFP4 原生 MSA 核函式、索引解碼上下文並行 (DCP)、雙批次重疊和 mono 核函式，整體性能提升 2-3 倍
- **代理工作負載測試**：NVIDIA GB300 達 418.9 tok/s 每使用者，Rubin 達 724.9 tok/s，AMD MI355X 達 133.3M tokens/$ TCO
- **Day-0 RL 支援**：整合 veRL、FSDP2 和 LoRA，支援 NVFP4 Checkpoint 的端到端強化學習

## 結論
vLLM 已全面支援 MiniMax-M3.1-Flash，提供多平台優化，可立即部署使用。預製映像檔已發布，NVIDIA 和 AMD 用戶均可使用，模型將在一週後透過 nightly PyPI wheel 提供完整支援。

---

快速開始：
- NVIDIA: `vllm/vllm-openai:minimax-m31-flash`
- AMD: `vllm/vllm-openai-rocm:minimax-m31-flash`

完整食譜可參考 vLLM Recipes，Checkpoints 可於 Hugging Face 獲取。
