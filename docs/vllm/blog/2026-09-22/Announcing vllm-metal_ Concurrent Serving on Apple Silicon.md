# Announcing vllm-metal: Concurrent Serving on Apple Silicon

- **來源**: vLLM Blog
- **發布日期**: 2026-09-22
- **原文連結**: https://vllm.ai/blog/2026-09-22-vllm-metal-v0-28-0

## 核心主題
vllm-metal 將 vLLM 的排程器、分頁 KV 快取和 OpenAI 相容伺服器移植到 Apple Silicon，使用 MLX 和 Metal 處理執行，實現高效並發服務。

## 關鍵重點
- vllm-metal 整合了 vLLM 的 V1 排程器、分頁 KV 區塊管理和分塊預填充功能，同時使用 MLX 執行模型，支援多模型並發處理。
- 支援批次多令牌預測 (MTP)、GGUF 和混合模型，並針對 M5 晶片優化預填充速度。
- 透過 Homebrew 安裝，提供 OpenAI 相容伺服器介面，可與各種編碼代理和工具整合。
- 在並發負載測試中，vllm-metal 在 Qwen3.8-27B 和 Gemma 4 E4B 模型上展現優異的 TTFT 和延遲表現。
- 支援混合模型對話歷史重疊，可重用先前輪次的計算區塊。

## 結論
vllm-metal 為 Apple Silicon 提供了高效、相容且易於使用的本地推理解決方案，特別適合需要高並發處理能力的場景。
---

檔案已成功儲存至指定路徑。