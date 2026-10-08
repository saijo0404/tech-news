# DeepSeek-V4.1-Flash on vLLM: 5x Agentic Throughput Since Day 0

- **來源**: vLLM Blog
- **發布日期**: 2026-10-07
- **原文連結**: https://vllm.ai/blog/2026-10-07-deepseek-v41-flash

## 核心主題
vLLM 團隊通過實現 SWA bounded replay 和整合 DeepSeek 的新核芯，在 DeepSeek-V4.1-Flash 模型上實現了顯著的性能提升。

## 關鍵重點
- **SWA bounded replay 優化**：結合 CUDA graphs 實現了約 30% 的首次 token 時間(TTFT) 降低，透過只重播最後 128 個 token 並剪輯 SWA 視窗，大幅減少預填充計算量。
- **新核芯整合**：整合了 MegaAttention、Mega-mHC、Mega-Gate 和 DeepSelect 等新核芯，其中 MegaAttention 支援 NVFP4 壓縮 KV，Mega-mHC 將 mHC 鏈條融合為單一核芯。
- **代理服務性能提升**：在 SemiAnalysis AgentX benchmarks 上，低併發場景下性能提升 1.9 倍，高併發場景下吞吐量提升 5.3 倍。
- **記憶體效率優化**：透過 Compressed Sparse Attention 2、FP4 KV cache 和層間 KV cache 共享，將全局 KV 佔用降至每 token 890 bytes。
- **Engram 優化**：支援透明巨頁(THP) 和異步預取，使 KV cache 外存查詢速度提升 10 倍。

## 結論
透過模型層面與系統層面的優化協同，vLLM 成功將 DeepSeek-V4.1-Flash 的代理服務性能提升 5 倍，特別是在高併發場景下表現突出，同時保持了極佳的記憶體效率和推理品質。

---