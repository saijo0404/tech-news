# From Day 0 to Production SLAs: Serving GLM-5.2 on 24 NVIDIA B300 GPUs with vLLM

- **來源**: vLLM
- **發布日期**: 2026-07-23
- **原文連結**: https://vllm.ai/blog/2026-07-23-glm-5.2-nvfp4-b300-pd

## 核心主題
DaoCloud 團隊成功在 24 張 NVIDIA B300 GPU 上部署 GLM-5.2-NVFP4 模型，透過分散式架構優化將 TPOT 從 40ms 降至 17ms，達成生產 SLA 目標。

## 關鍵重點
- **架構設計**：採用 4-Prefill + 1-Decode 分散式架構，使用 GLM-5.2-NVFP4 量化版本，解決 P/D 交接處混合批次問題
- **性能優化**：透過 Model Runner V2（降低 11% TPOT）、FlashInfer NVLink A2A 後端（降低 4% TPOT）和 CUDA Graph 模式優化，將平均 TPOT 從 40ms 優化至 17ms
- **架構決策**：選擇 TP1 DP4 EP 架構而非 TP1 DP2 EP，以保留 4 GPU 的 KV Cache 容量（犧牲 8% 效能換取功能完整性）
- **記憶體修復**：發現並修復 vLLM 容器記憶體洩漏問題（Mamba 層無時不一致閘控機制），已合併至 vLLM 主分支
- **品質驗證**：LongBench V2 得分 64.01，證明速度提升未犧牲輸出品質

## 結論
透過一系列針對 SLA 的優化措施，包括分散式架構設計、記憶體管理修復和性能優化，成功在生產環境中實現了高性能且符合服務等級協議的 GLM-5.2 服務。完整部署配置可直接用於 v0.26.0。

---

*本文摘要基於 DaoCloud 團隊在 vLLM 官方部落格發表的技術文章，所有優化措施和修復已合併至 vLLM 主分支。*
