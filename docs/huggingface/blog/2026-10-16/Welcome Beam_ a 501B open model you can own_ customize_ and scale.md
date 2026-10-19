# Welcome Beam: a 501B open model you can own, customize, and scale

- **來源**: Hugging Face Blog
- **發布日期**: 2026-05-27
- **原文連結**: https://huggingface.co/blog/reflection-beam

## 核心主題
Beam 是 Reflection 實驗室開發的 501B 參數混合專家(MoE)開源模型，提供高度可定制的部署方案與工具呼叫能力。

## 關鍵重點
- **模型架構**：501B 參數混合專家模型，每 token 僅 23B 活躍參數，52 層架構，支援 1M tokens 上下文長度
- **授權與獎勵**：Apache 2.0 開放授權，最佳專案可獲得 $10,000 Hub 信託獎勵
- **硬體部署**：支援 Blackwell (B300) 和 Hopper (H200) 硬體，提供 NVFP4 (280GB) 和 FP8 檢查點
- **訓練方法**：支援 SFT (TRL) 和 GRPO (Miles) 訓練，可進行 LoRA 微調
- **實際應用**：已實現 BeamSpeak 語音轉文字、多代理協作、決策模型訓練等案例
- **工具支援**：提供 Rust 基礎設施、transformers、vLLM、SGLang 原生支援

## 結論
Beam 模型提供高度可定制的開源解決方案，適合開發者和企業部署，並鼓勵社群分享專案以獲得獎勵。
---