# Native-speed vLLM transformers modeling backend

- **來源**: Hugging Face Blog
- **發布日期**: 2026-07-08
- **原文連結**: https://huggingface.co/blog/native-speed-vllm-transformers-backend

## 核心主題
vLLM 現在可以自動利用 transformers 實現來獲得與自實作相當甚至更快的推理速度，模型作者無需手寫優化代碼即可受益。

## 關鍵重點
- 使用 `--model-impl transformers` 旗標即可讓 vLLM 自動利用 transformers 建模後端，無需手寫任何優化代碼
- 在三個不同規模的 Qwen3 模型（4B、32B、235B）上測試，transformers backend 的效能達到或超越原生 vLLM 實作
- 使用 torch.fx 進行靜態分析，動態應用推理特定的層融合（如 Expert Parallelization、MergedColumnParallelLinear 等）來優化效能

## 結論
模型作者現在可以透過 transformers 庫直接獲得原生 vLLM 推理速度，無需額外優化工作，同時仍可保留訓練/評估/RL 滾動的兼容性。

---