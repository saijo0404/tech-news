# Serving Reflection Beam on vLLM from Day 0

- **來源**: vLLM Blog
- **發布日期**: 2026-10-16
- **原文連結**: https://vllm.ai/blog/2026-10-16-reflection-beam

## 核心主題
vLLM 從第一天起就完整支援 Reflection Beam 模型，並針對 NVIDIA Blackwell 進行優化，提供完整的推理、工具調用與結構化輸出功能。

## 關鍵重點
- **Agent 驅動優化**：程式碼代理自動優化模型，使 batch-1 解碼速度快 2.71 倍，prefill 速度快 1.87 倍。
- **DFlash2 推論加速**：支援 DFlash2 草稿頭，單請求在 TP8 上達 708 tokens/s，並透過自适应驗證在高併發時提升 10.8% 吞吐量。
- **完整功能支援**：支援 Tensor、Data 或 Expert Parallelism，並與 SkyRL 團隊合作實現 RL 從第一天起就可用。

## 結論
vLLM 透過自動化優化與專用硬體支援，成功將 Reflection Beam 這個 501B 參數的 MoE 模型在第一天就完整支援，並在高併發場景下展現優異性能。
---
