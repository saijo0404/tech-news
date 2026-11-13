# DeepSeek-V4.1-Flash on Vera Rubin NVL72: 58x Throughput vs. GB300 NVL72 at 387 tokens/s

- **來源**: vLLM Blog
- **發布日期**: 2026-11-12
- **原文連結**: https://vllm.ai/blog/2026-11-12-deepseek-v41-flash-vera-rubin

## 核心主題
vLLM 在 NVIDIA Vera Rubin NVL72 機架上運行 DeepSeek-V4.1-Flash 模型，實現了相比 GB300 NVL72 58倍的吞吐量提升，透過針對 Rubin 硬體特性的深度優化達到極致性能。

## 關鍵重點
- **單用戶性能突破**：單個 GPU 達到 1.7M tokens/s，每個用戶 387 tokens/s，是 GB300 NVL72 的 58倍；峰值吞吐量達 2.52M tokens/s，單用戶 P90 達 1,810 tokens/s
- **Rubin 硬體特性優化**：針對 Rubin 的分裂記憶體架構和 SM107 更寬的 MMA 指令進行核函式重構，使 DEP2 prefill 步驟快 28%、DEP decode 步驟快 25%
- **跨機架記憶體共享**：利用 72 GPU 共享單一 NVLink 架構，實現跨托盤 TP8 部署，KV Cache 和 Engram 表跨 GPU HBM 共享，大幅提升高併發場景下的 prefix hit rate（96.5–97%）
- **專用低延遲解碼路徑**：針對最低延遲需求，實現跨操作者融合、計算與通信重疊，單用戶 P50 從 1,117 tokens/s 提升至 1,844 tokens/s

## 結論
透過深度針對 Vera Rubin NVL72 硬體特性（分裂記憶體、SM107 寬 MMA、NVLink 統一記憶體）的優化，vLLM 在 DeepSeek-V4.1-Flash 上實現了前所未有的性能突破，為下一代 AI 推理服務提供了新的性能基準。

---
*此摘要基於 vLLM Blog 於 2026 年 11 月 12 日發布的文章整理*
