# Experience and Lessons Learned from Serving Multi-Stage Qwen3-Omni in vLLM-Omni

- **來源**: vllm.ai
- **發布日期**: 2026-07-01
- **原文連結**: https://vllm.ai/blog/2026-07-01-qwen3-omni-optimization

## 核心主題
vLLM-Omni 透過多階段優化技術（CUDA Graph、異步分塊、階段複製等）大幅提升 Qwen3-Omni 的推理效能，吞吐量提升 432%，首音延遲大幅降低。

## 關鍵重點
- **三階段管道架構**：Qwen3-Omni 採用 Thinker（多模態理解 + 文字生成）、Talker（隱藏狀態轉 RVQ 編碼器代碼）、Code2Wav（代碼轉音頻波形）三階段架構，各階段採用獨立批處理策略
- **CUDA Graph 優化**：三階段皆採用圖優化，TPOT 降低 53%，吞吐量提升 299%
- **異步分塊與輸出**：Async Chunk 技術使首音延遲從 5884ms 降至 655ms，Async Output 將 RTF 降至 0.47
- **階段複製策略**：Talker 與 Code2Wav 各複製 2 份，解決高併發時瓶頸，64 並發時達 11.7 req/s（比 Batch 基線提升 5.4 倍）
- **熱路徑清理優化**：優化 Talker 解碼循環，減少冗餘 Connector 傳輸；單一 GPU 部署預設使用 uni executor；優化 Connector payload 組建；保留 GPU 內中間張量

## 結論
透過多層優化技術組合（CUDA Graph、Async Chunk、Async Output、Stage Replicas、熱路徑清理），vLLM-Omni 成功將 Qwen3-Omni 的推理效能大幅提升，吞吐量從 2.2 req/s 提升至 11.7 req/s，RTF 從 1.15 降至 0.47，TTFP 從 5884ms 降至 632ms，為多階段多模態模型服務提供高效解決方案。

---

部署方式：
```bash
vllm serve Qwen/Qwen3-Omni-30B-A3B-Instruct \
  --omni \
  --port 8091
```
請求端點：`/v1/chat/completions`，可設定 modalities 為 `["text"]` 或 `["text", "audio"]`。
