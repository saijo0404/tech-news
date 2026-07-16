# vime + ROCm: End-to-End RL Post-Training on AMD Instinct™ GPUs

- **來源**: vLLM Blog
- **發布日期**: 2026-07-10
- **原文連結**: https://vllm.ai/blog/2026-07-10-vime-rocm

## 核心主題
vLLM 團隊正式宣布 vime 框架對 AMD Instinct MI355X GPU 的 ROCm 支援，實現端到端強化學習後訓練工作流的原生支援。

## 關鍵重點
- vime 採用三階段解耦設計（訓練、推論、資料緩衝），現在可在 ROCm 上完整運行，無需額外代碼修改
- AMD Instinct GPU 擁有大統一 HBM 記憶體（MI355X 達 288 GB）和高記憶體頻寬（8 TB/s），適合 RL 工作負載
- 支援 Megatron-LM 訓練後端和 vLLM 推論後端，提供 colocated 模式以減少記憶體競爭
- 提供預構建容器（vllm/vime-rocm），無需從源代碼編譯即可啟動完整 RL 訓練工作流
- 性能測試顯示 Qwen3-8B 模型在 MI355X 上可維持約 4,100 tokens_per_gpu_per_second 的通量，logprob 差異穩定在 0.012 左右

## 結論
vime 與 AMD 團隊的合作使 RL 後訓練工作流能夠在 AMD 硬體上原生運行，為使用 ROCm 的團隊提供了完整的工具鏈支持，包括預構建容器、訓練腳本和性能優化建議。

---