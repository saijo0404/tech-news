# EAGLE-3 Speculative Decoding on AMD Instinct GPUs: Training and Serving with vLLM and AMD Quark

- **來源**: vLLM Blog
- **發布日期**: 2026-07-13
- **原文連結**: https://vllm.ai/blog/2026-07-13-eagle-3-amd-instinct

## 核心主題
vLLM 團隊展示了如何在 AMD Instinct GPU 上完整實現 EAGLE-3 猜測解碼（speculative decoding）技術，結合 AMD Quark 量化與 vLLM 推理引擎，實現從訓練到部署的全流程優化。

## 關鍵重點
- EAGLE-3 使用目標模型的內部特徵（低、中、高層次隱藏狀態）訓練草稿模型，比傳統小語言模型草稿具有更高的接受率
- AMD Quark 提供 Day-0 MXFP4/FP8 量化支持，讓主流 LLM 在發布時即可直接使用硬件優化版本
- vLLM 中心化的訓練管道：用目標模型生成 on-policy 數據、提取隱藏狀態、在循環中進行 serve-eval 評估，確保訓練與部署一致
- 在 Kimi-K2.5 和 MiniMax-M2.5 模型上測試，Kimi-K2.5 獲得 1.69x-2.00x 吞吐量提升，MiniMax-M2.5 獲得 1.38x-1.79x 提升
- 接受長度在 1K 到 32K 上下文範圍內基本穩定，證明速度提升不會因長上下文而衰減

## 結論
AMD Quark 團隊通過單一團隊負責目標模型量化、草稿模型訓練和 vLLM 部署，為 AMD Instinct GPU 用戶提供了一站式的猜測解碼解決方案，無需手動組裝 CUDA 中心化工具。

---