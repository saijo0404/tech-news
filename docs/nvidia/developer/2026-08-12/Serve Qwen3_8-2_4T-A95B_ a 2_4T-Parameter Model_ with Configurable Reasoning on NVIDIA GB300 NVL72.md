# Serve Qwen3.8-2.4T-A95B, a 2.4T-Parameter Model, with Configurable Reasoning on NVIDIA GB300 NVL72

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-08-12
- **原文連結**: https://developer.nvidia.com/blog/serve-qwen3-8-2-4t-a95b-a-2-4t-parameter-model-with-configurable-reasoning-on-nvidia-gb300-nvl72/

## 核心主題
阿里巴巴發布了 Qwen3.8-2.4T-A95B 最大開源權重模型，並介紹了如何在 NVIDIA GB300 NVL72 平台上部署該模型，實現高吞吐量推理。

## 關鍵重點
- **模型架構**: 2.4T 總參數的混合專家 (MoE) 架構，95B 每 token 激活，結合全注意力與線性注意力，支援 100 萬 token 上下文窗口
- **推理性能**: 在 NVIDIA GB300 NVL72 上，FP8 精度下首日即達每秒 4K+ token 吞吐量，支援 128K 輸出長度
- **可配置推理**: 提供 low/high/xhigh 三級推理控制，開發者可根據任務需求調整推理深度與計算成本
- **部署方案**: 支援 SGLang、vLLM、NVIDIA Dynamo 等多個推理堆疊，並提供模型無服務 (NIM) 部署選項
- **微調支援**: 透過 NVIDIA NeMo AutoModel 支援 Day-0 微調，無需模型轉換即可進行全量 SFT 或 LoRA 微調

## 結論
NVIDIA 與開源生態合作，透過優化核心函式、推理時序與分佈式服務配方，使 2.4T 參數開源模型能在生產環境中以高吞吐量、低延遲運行，為 AI 工廠提供可擴展的推理解決方案。
---
