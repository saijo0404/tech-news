# Day 0 Support for Qwen3.8-2.4T-A95B on vLLM

- **來源**: vLLM Blog
- **發布日期**: 2026-08-12
- **原文連結**: https://vllm.ai/blog/2026-08-12-qwen3.8

## 核心主題
vLLM 正式宣布對 Qwen3.8-2.4T-A95B 模型提供 Day-0 支援，這是 Qwen 系列中第一個達到 Qwen-Max 等級的開源模型，基於 Qwen 3.5 架構，無需架構修改即可在 vLLM 上運行。

## 關鍵重點
- **精確度選項豐富**：提供 FP8、BF16、NVFP4 和 MXFP4 四種精確度檢查點，MXFP4 版本可大幅降低記憶體和頻寬消耗。
- **硬體支援廣泛**：經過 NVIDIA 和 AMD 硬體驗證，2.4 兆參數稀疏 MoE 模型（512 專家）需至少兩節 B300/MI355X 節點（FP4 量化版本可單節點運行）。
- **性能優化顯著**：與 NVIDIA 和 AMD 合作開發優化核，包括 Linear Attention、GQA、Dense GEMM 和 MoE 路由等，並支援 AITER-fused 核以減少開銷。
- **FP4 量化效果優異**：通過 Round-to-Nearest 量化和激活校準，在 GSM8K 和 AIME25 等 benchmarks 上表現優於 FP8，同時大幅降低推理成本。
- **快速啟動指南**：提供完整的 Docker 啟動命令和部署建議，支援自動工具選擇和推理解析器。

## 結論
vLLM 與 Inferact 團隊成功實現了 Qwen3.8-2.4T-A95B 模型的 Day-0 支援，通過多精確度選項和硬體優化，為開發者提供了靈活的部署方案，特別適合需要高推理性能和大規模開源模型的場景。

---