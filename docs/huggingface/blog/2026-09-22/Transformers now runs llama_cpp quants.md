# Transformers now runs llama_cpp quants

- **來源**: Hugging Face
- **發布日期**: 2026-09-22
- **原文連結**: https://huggingface.co/blog/transformers-llama-cpp-quants

## 核心主題
Hugging Face 的 Transformers 庫新增對 llama.cpp GGUF 量化模型的支援，讓開發者能在本地機器上透過熟悉的 PyTorch/transformers API 運行 GGUF 模型，並優化模型生成循環以提升性能。

## 關鍵重點
- 新增 llama.cpp GGUF 量化模型支援，可透過 PyTorch API 直接運行，無需額外配置
- 支援 Apple Silicon 優化，使用 ggml 的 Metal 核加速推理
- 提供量化選擇建議，推薦從 Q4_K_M 開始，可根據記憶體調整為 Q5_K_M 或 Q6_K
- 優化模型生成循環，提前移除無效注意力掩碼並延遲停止檢查，減少同步點提升並行效率
- 可透過 transformers serve 提供 OpenAI 相容 API，連接 Jan/Pi 等客戶端
- 保留 PyTorch 生態，可進行中間激活檢查、模型修改、評估及微調
- 性能表現與 llama.cpp 相當，在 MacBook Pro M2 Max 上測試驗證

## 結論
此整合讓 GGUF 模型能更便捷地在 Python/PyTorch 環境中運行，同時保持 llama.cpp 的高效推理性能。後續將擴展至更多模型架構（如 Qwen3.5 dense 和 MoE 架構）及更多功能（如 generate_batch 支援）。

---