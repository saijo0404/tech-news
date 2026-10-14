# Run fast, private agents on-device with LFM2.5-24B-A2B

- **來源**: Hugging Face
- **發布日期**: 2026-10-13
- **原文連結**: https://huggingface.co/blog/LiquidAI/lfm25-24b-a2b

## 核心主題
LFM2.5-24B-A2B 是一個具有 240 億參數但僅有 20 億活躍參數的推理模型，專為快速、私密的本地設備代理設計。它會在回答前進行推理，調用工具，並在流行的代理框架內處理多步驟任務。

## 關鍵重點
- **高效能 MoE 架構**：僅有 2B 活躍參數，使每個推理 token 成本更低，可持續在本地硬體上運行代理
- **最佳級代理表現**：在工具使用和代理任務上與 Qwen3.6-35B-A3B（總參數和活躍參數多 50%）具有競爭力，在 LiveClaw 上得分 48.09 對比 38.19
- **快速推理速度**：Apple M5 Max 上達 184 tok/s，單張 NVIDIA B300 GPU 上達 21K tok/s
- **擴展的上下文能力**：上下文窗口從 32K 擴展