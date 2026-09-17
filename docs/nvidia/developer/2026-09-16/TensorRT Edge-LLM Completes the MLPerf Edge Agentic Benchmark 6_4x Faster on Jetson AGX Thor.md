# TensorRT Edge-LLM Completes the MLPerf Edge Agentic Benchmark 6.4x Faster on Jetson AGX Thor

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-09-16
- **原文連結**: https://developer.nvidia.com/blog/tensorrt-edge-llm-completes-the-mlperf-edge-agentic-benchmark-6-4x-faster-on-jetson-agx-thor/

## 核心主題
NVIDIA TensorRT Edge-LLM 在單一 Jetson AGX Thor 開發套件上運行 Qwen3.6-27B 模型，在 MLPerf Inference v6.1 Edge Agentic 測試中實現 6.4 倍性能提升，完成所有 1,007 次轉折僅需 24 分 36 秒。

## 關鍵重點
- **NVFP4 量化加速**: 使用 NVFP4 量化權重和激活值，FP8 KV 快取，大幅降低記憶體佔用並提升解碼速度
- **KV 快重用**: 約 96% 的提示 token 從熱快取中服務，僅需預填充約 0.5M 的 token，減少重複計算
- **樹狀多 token 預測**: 採用 8 步驟、top-2、16 節點驗證樹的 MTP 實現，比線性 MTP 額外提升約 40% 解碼性能
- **高吞吐量與準確性**: 輸出吞吐量達 52.33 tokens/秒，BFCL 整體準確率 87.94%
- **6.4 倍性能提升**: 相比 llama.cpp 參考實現（2 小時 37 分鐘），完成時間縮短至 24 分 36 秒

## 結論
TensorRT Edge-LLM 通過量化、快重用和多 token 預測等優化技術，為邊緣設備上的 AI 代理推理提供了高效解決方案，顯著提升了 Jetson AGX Thor 平台上的 LLM 推理性能，為未來 AI 代理從雲端數據中心向車輛、機器人等邊緣設備的部署奠定了技術基礎。

---

*本文摘要基於 NVIDIA Technical Blog 於 2026 年 9 月 16 日發布的技術文章。*