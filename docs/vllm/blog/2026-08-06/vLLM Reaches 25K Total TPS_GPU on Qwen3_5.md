# vLLM Reaches 25K Total TPS/GPU on Qwen3.5

- **來源**: vLLM Blog
- **發布日期**: 2026-08-06
- **原文連結**: https://vllm.ai/blog/2026-08-06-qwen35-25k-tps

## 核心主題
vLLM 團隊在 Qwen3.5 模型上實現了單 GPU 每秒 25,000 Tokens 的總吞吐量，通過優化混合注意力架構的預填充和分發服務。

## 關鍵重點
- **Blackwell 優化 GDN 預填充**: 引入針對 Blackwell GPU 的 FlashInfer GDN 核核，性能提升 1.02 至 5.78 倍，在 8×B200 系統上實現 5.92 倍性能提升
- **混合 KV 緩存與 GDN 狀態傳輸**: 實現了混合 SSM-注意力模型的異構傳輸，支持 Qwen3.5 的混合架構，通過 NIXL 連接器傳輸 KV 緩存和 Mamba 風格狀態
- **無競態異步排程**: 修復了 KV 區塊傳輸中的競態條件，使異步排程成為突破 25K TPS 的關鍵功能

## 結論
這些優化使 vLLM 能夠在 GB200 NVL72 系統上高效運行 Qwen3.5，為大模型服務提供了可重現的最佳實踐。準確率測試顯示所有配置均達到 88%，與聚合運行結果一致。

---