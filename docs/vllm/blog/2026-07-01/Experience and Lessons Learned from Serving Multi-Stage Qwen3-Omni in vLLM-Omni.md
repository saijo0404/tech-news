# Qwen3-Omni 在 vLLM-Omni 中的服務優化總結

- **來源**: vLLM Blog
- **發布日期**: 2026-06-29
- **原文連結**: https://vllm.ai/blog/2026-07-01-qwen3-omni-optimization

## 核心主題
vLLM-Omni 透過六層優化技術（階段分解、CUDA Graph、Async Chunk、Async Output、Stage Replicas、Hot-Path Cleanup）服務 Qwen3-Omni，將高併發下的語音生成效能從 2.2 req/s 提升至 11.7 req/s，並將語音延遲從 1.15 降至 0.47 倍。

## 關鍵重點
- **階段分解（Stage Decomposition）**：將 Thinker、Talker、Code2Wav 三個階段獨立為獨立的運行環境，可針對各階段採用不同的批處理、圖捕捉與設備佈局策略，避免單一策略限制整體效能。
- **CUDA Graph 圖捕捉**：針對三個階段的解碼路徑進行 CUDA Graph 捕捉，消除每步驟的 CPU 側核函式調用，使 req/s 從 2.2 提升至 8.6（+299%），audio RTF 從 1.15 降至 0.59。
- **Async Chunk 分階段交接**：取代完整載入屏障，採用分階段部分交接，使首語音延遲（TTFP）從 2790ms 大幅降至 655ms，是語音延遲最大的優化收益。
- **Async Output 非阻塞載入**：將載入組裝從解碼路徑移至非阻塞輸出，減少 GPU 等待時間，進一步降低 audio RTF 至 0.47。
- **Stage Replicas 階段複數化**：針對 Talker 與 Code2Wav 進行複數化（2× Talker + 2× Code2Wav），解決這些階段在高併發下成為瓶頸的問題，使吞吐量達到峰值 11.7 req/s。
- **Hot-Path Cleanup 熱路徑清理**：針對 Talker 解碼迴圈中的重複連接器流量、每步驟 torch.cat 與 CPU 序列化等模型內部成本進行優化，在長上下文單請求測試中，E2EL 從 21.28s 降至 7.37s，audio RTF 從 0.71 降至 0.28。

## 結論
vLLM-Omni 透過針對性優化每個階段，成功將 Qwen3-Omni 的語音生成效能大幅提升，在保持低延遲的同時實現高併發吞吐量。這種分階段、分策略的優化模式，為未來多階段 AI 系統的效能優化提供了可參考的架構設計模式。各層優化疊加使用，從僅能跟隨負載的管道轉化為擁有實時緩衝餘量的系統。CUDA Graph 與 Async Chunk 主導延遲降低，而 Async Output 與 Stage Replicas 則在高併發下提供吞吐量餘量。
---
