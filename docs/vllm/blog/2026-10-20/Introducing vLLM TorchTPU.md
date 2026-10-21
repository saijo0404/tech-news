# Introducing vLLM TorchTPU

- **來源**: vLLM Blog
- **發布日期**: 2026-10-20
- **原文連結**: https://vllm.ai/blog/2026-10-20-vllm-torchtpu

## 核心主題
vLLM 推出了 TorchTPU 後端，讓 vLLM 可以在 Google Cloud TPU 上運行，重用現有模型代碼，並提供優化的 TPU 推理性能。

## 關鍵重點
- vLLM TorchTPU 是一個外掛插件，自動集成到 vLLM 中，支持大多數現有模型無需修改代碼即可在 TPU 上運行
- 使用 Google 的 TorchTPU 堆疊和 Pallas 核，為注意力、混合專家和量化矩陣乘法提供手調優化
- 支持所有 vLLM 的並行化維度，包括張量並行、數據並行、管道並行、專家並行和前綴/解碼上下文並行
- 支持零拷貝 KV 緩存離線和分散式服務，利用 TPU Sync 庫實現低傳輸開銷
- 支持推測解碼和前綴緩存，包括 MTP、EAGLE-3、DFlash、DSpark 等技術
- 推薦使用 TPU v7x (Ironwood) 硬體，並提供貢獻者 TPU 時間池

## 結論
vLLM TorchTPU 為在 Google Cloud TPU 上運行大模型提供了開源解決方案，並計劃在模型發布當天就支持新模型，同時保持 vLLM 原有的易用性體驗。
---