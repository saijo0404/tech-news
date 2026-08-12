# Announcing Day-0 Support for NVIDIA Nemotron 3.5 Lightning on vLLM

- **來源**: vLLM Blog
- **發布日期**: 2026-08-10
- **原文連結**: https://vllm.ai/blog/2026-08-10-nemotron-3-5-lightning-vllm

## 核心主題
vLLM 正式宣布對 NVIDIA Nemotron 3.5 Lightning 模型提供 Day-0 支援，這是一個專為 Always-on 代理設計的混合 MoE 架構開源模型，提供 300 億總參數但每次只激活 30 億參數，支援多 Token 預測和推測解碼技術。

## 關鍵重點
- **混合 MoE 架構**: 30B 總參數，3B 活躍參數，每次 token 只激活 30 億參數，大幅提升效率
- **三種推測解碼技術**: 支援 Multi-Token Prediction (MTP)、DFlash 和 DSpark，可根據工作負載選擇最佳方案
- **高吞吐量**: 比類似規模開源模型快達 4 倍，適合高頻率代理任務
- **廣泛部署平台**: 支援 NVIDIA DGX Spark、H100、H200、A100、Jetson 等多種硬體平台
- **兩種精度版本**: 提供 BF16 和 NVFP4 兩種權重格式，滿足不同環境需求
- **最大上下文**: 支援最高 100 萬 token 的上下文長度
- **OpenAI 相容 API**: 可透過標準 API 部署並整合至現有代理框架

## 結論
vLLM 為 Nemotron 3.5 Lightning 提供了即時的 Day-0 支援，使開發者可以立即在生產環境中部署此模型，特別適合需要高吞吐量、高準確性代理任務的場景，包括個人助理、企業自動化系統和專業化代理應用。

---