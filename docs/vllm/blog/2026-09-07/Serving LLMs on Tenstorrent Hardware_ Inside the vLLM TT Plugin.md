# Serving LLMs on Tenstorrent Hardware: Inside the vLLM TT Plugin

- **來源**: vLLM Blog
- **發布日期**: 2026-09-07
- **原文連結**: https://vllm.ai/blog/2026-09-07-vllm-tt-plugin

## 核心主題
vLLM TT Plugin 透過標準插件機制將 Tenstorrent 加速器整合至 vLLM，支援多種 TT 前綴架構模型和多模態模型，並針對 Tenstorrent 的網狀架構特性進行特殊設計。

## 關鍵重點
- 支援 Llama 3.1/3.2/3.3、Qwen 系列、Mistral、Gemma 等 TT 前綴架構模型，以及 Llama 3.2 Vision、Qwen-VL 等多模態模型
- 採用階段式排程（prefill-only 或 decode-only），無混合批次，每個排程步驟必須是單一模式
- 單一進程 Lane 資料並行：Galaxy 模型採用單一引擎進程內含多個獨立排程器，每個 Lane 有自己的等待和執行佇列
- 裝置上採樣：可將採樣邏輯置於裝置內，減少 host 負擔，token 可能已經被選擇，host 無需看到 logits
- 採用編譯式執行：資料並行透過編譯的網狀程式實現，非 runtime 配置，支援 2 片 n300 至 32 片 Galaxy 網狀
- 採樣機制採用混合採樣路徑，支援 decode/host overlap，但僅為異步主機讀回（非異步執行）
- 需先安裝 TT-Metal 環境，克隆並執行 `docs/install-vllm-tt.sh` 腳本，使用 `examples/server_example_tt.py` 進行測試
- 模型限制：需宣告 `supports_async_decode` 才能啟用異步解碼，目前不支援 Speculative decoding、LoRA、Prompt logprobs、多主機服務

## 結論
vLLM TT Plugin 成功透過標準插件機制整合 Tenstorrent 硬體，提供與 GPU 相似的 serving 表面，同時針對 Tenstorrent 的網狀架構特性進行特殊設計。未來改進方向包括擴大異步解碼覆蓋範圍、擴展前綴快取、支援 Speculative decoding 和實現多主機服務。
---
