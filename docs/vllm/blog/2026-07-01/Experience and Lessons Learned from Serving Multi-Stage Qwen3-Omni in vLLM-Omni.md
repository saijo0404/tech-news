---
# Experience and Lessons Learned from Serving Multi-Stage Qwen3-Omni in vLLM-Omni

- **來源**: vLLM Blog
- **發布日期**: 2026-07-01
- **原文連結**: https://vllm.ai/blog/2026-07-01-qwen3-omni-optimization

## 核心主題
vLLM-Omni 團隊分享在 vLLM-Omni 中部署 **Qwen3-Omni-30B-A3B** 多模態模型（結合多模態理解與語音生成）的實戰經驗——透過六層優化堆疊（階段分解、CUDA Graph、非同步 Chunk、非同步輸出、階段副本、熱路徑清理）將每請求吞吐量從 **2.2 req/s 提升至 11.7 req/s**（約 5.4 倍），平均音訊首幀延遲（TTFP）從 5884ms 降至 **631ms**，音訊 RTF 從 1.15 降至 **0.47**。

## 關鍵重點
- **六層優化堆疊與階段解耦**：Qwen3-Omni 由三個計算特徵迥異的階段組成——**Thinker**（多模態理解 + 文字生成）、**Talker**（隱藏狀態 → RVQ 編碼器代碼）、**Code2Wav**（代碼 → 語音波形）。階段分解解除耦合，讓每階段有獨立排班、圖表策略與副本設定；CUDA Graph 針對三階段分別 capture（Thinker 外層圖表、Talker 外層圖表 + torch.compile 編譯內部編碼器、Code2Wav 內部 CUDAGraphDecoderWrapper），使吞吐量躍升 299%；非同步 Chunk 以流水線部分傳遞取代全負載屏障，帶來最大單次 TTFP 改善（-77%）。
- **非同步輸出、階段副本與熱路徑清理**：非同步輸出將 connector payload 建構與階段傳遞解耦，步間間隙縮至約 41 µs，RTF 降至 0.47；階段副本僅針對飽和的 Talker（×2）與 Code2Wav（×2）水平擴展，Thinker 保持單一副本避免記憶體浪費，吞吐量推至 11.7 req/s；熱路徑清理針對模型內部重複開銷，包含連接器 O(1) 傳遞、payload 建構優化、編碼器預測器重寫、GPU 駐留解碼狀態等六項改進，長上下文端到端延遲從 21.28s 降至 7.37s。
- **基準測試總覽（併發 1/16/32/64）**：在各併發層級下，六層優化逐層疊加產生複合效應——CUDA Graph 貢獻最大單次吞吐量躍升（~4×），Async Chunk 貢獻最大單次 TTFP 降幅，Async Output 與 Stage Replicas 在高併發（32/64）下提供額外吞吐量緩衝。最終 RTF 從低於實時的 1.15 推進至遠超實時的 0.47，證明系統從「負載下勉強維持」升級為「擁有充裕緩衝空間」。

## 結論
Qwen3-Omni 的部署經驗證明了多階段模型優化的核心原則：**沒有單一優化能單獨解決所有問題，每層優化針對不同瓶頸，疊加後才能產生複合效應**。這套六層優化堆疊提供了一個系統化、可量化的實戰藍圖——從階段解耦、圖表優化、非同步流水線、精確擴展到模型內部熱路徑微調，任何需要部署多階段 AI 模型的團隊均可參考。

---
