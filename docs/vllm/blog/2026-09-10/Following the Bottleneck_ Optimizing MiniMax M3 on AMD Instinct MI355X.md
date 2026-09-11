# Following the Bottleneck: Optimizing MiniMax M3 on AMD Instinct MI355X

- **來源**: vLLM Blog
- **發布日期**: 2026-09-10
- **原文連結**: https://vllm.ai/blog/2026-09-10-minimax-m3-mi355x

## 核心主題
這篇文章介紹了 vLLM 如何針對 MiniMax M3 模型在 AMD Instinct MI355X 晶片上的優化進展，透過五個關鍵問題（形狀、重複工作、資料移動、快徑執行、佇列成長）來追蹤並解決效能瓶頸。

## 關鍵重點
- **形狀分析與分發策略**：根據實際運行的局部形狀（local shape）動態調整 tile 選擇與後端分發，在低併發情況下提升 1.08-1.46 倍，並修正 TP 分發對算子圖的影響。
- **共享專家融合（Shared Expert Fusion）**：將共享專家併入路由專家表，透過分組 GEMM 同時處理路由與共享專家，移除重複啟動與中間流量，輸出吞吐量提升 30.2%（併發 1）至 5.6%（併發 128）。
- **索引共享與頁面表技術**：透過索引共享降低 TPOT 10%-4%，並使用頁面表技術避免 KV 資料複製，實現「傳遞視圖而非複製容器」的效能優化。
- **嚴格區分配置與執行**：修正 INT4 QuickReduce 誤用問題，強調「configured ≠ eligible ≠ executed」，必須透過分發追蹤或 profiler 驗證快徑是否真正執行。
- **EAGLE3 猜測解碼整合**：在 TP4/EP1 架構下成功整合 EAGLE3，達致 682.4 output tokens/s/GPU，並修正 cache key 與 draft 配置不匹配問題。

## 結論
優化過程證明追蹤瓶頸是持續性的，每個改進都帶來新的瓶頸。透過系統化的五問法（形狀、重複工作、資料移動、快徑執行、佇列成長），團隊成功將 MiniMax M3 在 MI355X 上的吞吐量提升 3.14-4.45 倍，並為後續模型優化建立可重複的方法論。

---