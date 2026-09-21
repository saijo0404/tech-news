# Benchmarking LLM Inference at Scale with AIPerf

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-09-18
- **原文連結**: https://developer.nvidia.com/blog/benchmarking-llm-inference-at-scale-with-aiperf/

## 核心主題
介紹 NVIDIA AIPerf 工具，取代 GenAI-Perf，提供多工架構以進行大語言模型推理效能測試。

## 關鍵重點
- AIPerf 採用多工架構，避免客戶端成為瓶頸，支援超過 15 種端點類型和公開數據集
- 支援可配置的到達模式（常數、Poisson、Gamma 分佈），可調整突發性以匹配生產流量特徵
- 提供核心指標（TTFT、ITL、請求延遲、輸出 token 吞吐量）的百分位數分解和 GPU 遥測數據

## 結論
AIPerf 是進行大語言模型推理效能測試的理想工具，提供準確、可重複且易於配置的基準測試解決方案。
---