# Inkling 2 Mini on vLLM: Day-0 Support for a Looped Model

- **來源**: vLLM Blog
- **發布日期**: 2026-11-20
- **原文連結**: https://vllm.ai/blog/2026-11-20-inkling2-mini

## 核心主題
vLLM 正式支援 Thinking Machines 推出的 Inkling 2 Mini 循環模型，提供 Day-0 支援，包括循環層、多模態 MoE 架構、DSpark 推論加速器以及強化學習支援。

## 關鍵重點
- **循環模型架構**：Inkling 2 Mini 是循環模型，其中間 12 層（第 6-17 層）會執行三次循環，每層有自己的 KV Cache 和來自前一次的閹控訊息，每層執行時讀取前一次的訊息
- **模型規格**：總參數 26B，活躍參數 3.5B，支援 1M token 上下文，內建 DSpark 推論加速器，使用 NVFP4 專家（最後 4 層使用 MXFP8）
- **硬體支援**：在 NVIDIA Blackwell、Hopper 和 DGX Spark 上提供 Day-0 優化支援，vLLM 將每個循環層的 Cache 視為普通 Cache 層管理，融合訊息讀取和控制器
- **強化學習支援**：支援 SkyRL 進行強化學習訓練，提供 Docker 映像包 vllm/vllm-openai:inkling-2-mini
- **變數循環研究檢查點**：還支援 TML-d24-varloop-research，允許使用者自訂循環次數（至少 1 次，預設 3 次）和是否共享 KV Cache 的選項

## 結論
vLLM 成功實現了對 Inkling 2 Mini 循環模型的完整支援，包括高性能推論和準確性驗證，為多模態循環模型服務提供了新的標準。測試顯示，在 GB200 GPU 上，3 次循環的推論時間約為 3.85ms（單批次）至 8.11ms（32 批次），準確性與參考實現一致。

---