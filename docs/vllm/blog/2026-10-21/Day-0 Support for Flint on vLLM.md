# Day-0 Support for Flint on vLLM

- **來源**: vLLM Blog
- **發布日期**: 2026-10-21
- **原文連結**: https://vllm.ai/blog/2026-10-21-flint

## 核心主題
vLLM 從第一天起就支援 Recursive 的 Flint 模型，提供 NVFP4 和 BF16 兩種檢查點，在單張 GB200 GPU 上可達約 500 tokens/s 的解碼速度，即使處理 100K tokens 的上下文。

## 關鍵重點
- **模型架構特色**：Flint 是 40B 參數的 MoE 模型，每 token 僅激活約 2.5B 參數，採用滑動視窗注意力機制，大部分層只關注局部上下文，僅 14 層處理完整上下文，大幅降低 KV cache 成本。
- **性能優化成果**：通過一系列針對小批次優化，將 NVFP4 解碼從 4.81ms 降至 1.78ms（2.7 倍提升），BF16 解碼從 3.53ms 降至 2.34ms（1.5 倍提升），8K token 預填充從 207ms 降至 145ms（1.4 倍提升），總解碼步數從 1,096 個核降至 346 個。
- **使用方式**：提供 day-0 Docker 影像 vllm/vllm-openai:flint，支援 x86_64 和 arm64 架構，CUDA 13.0，可透過 Docker 或 vllm serve 命令啟動，支援 NVFP4（GGUF）和 BF16 兩種檢查點。
- **準確性保證**：所有 Flint 核函數遵循參考實現的取捨點，在 GSM8K、GPQA-Diamond、長上下文 MRCR 和工具調用套件上準確性一致。
- **工具調用支援**：Flint 發出 GLM-4.7 風格的工具調用和思考區塊，使用 glm47 解析器，支援自動工具選擇。

## 結論
vLLM 成功實現了對 Flint 模型的完整支援，從第一天起即可使用，並通過針對小批次和 MoE 架構的優化，顯著提升了性能。用戶可以透過 Docker 或 vllm serve 輕鬆啟動，並獲得與參考實現一致的準確性。

---