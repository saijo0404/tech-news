# 3 Ways to Boost MoE Inference on NVIDIA DGX Spark

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-10-27
- **原文連結**: https://developer.nvidia.com/blog/3-ways-to-boost-moe-inference-on-nvidia-dgx-spark/

## 核心主題
這篇文章介紹了如何在 NVIDIA DGX Spark 平台上提升混合專家（MoE）模型的推理性能，通過三種關鍵優化技術實現顯著的性能提升。

## 關鍵重點
- **Humming MXFP4 MoE 後端**：用 Humming 替換 FlashInfer MXFP4 後端，將每輸出 token 時間從 27.71ms 降至 25.35ms，吞吐量提升 9.3%。
- **線上 FP8 LM head 量化**：將輸出層權重從 BF16 量化為 FP8，讀取量減少一半，結合 Humming 後吞吐量提升 21.7%。
- **多 token 預測（MTP）猜測解碼**：使用 NEXTN 層進行多 token 預測，每輪接受 3.90 個 token，吞吐量提升 185.1%。

## 結論
在完整 GSM8K 測試集上，這三項優化共同使解碼吞吐量提升 42.5%，平均延遲降低 24.5%，且無可檢測的準確性變化。部署時需確保所有優化正確啟用，否則可能導致性能低於基準。

---

最後，將完整的摘要結果直接儲存為檔案：/yijun/Project/tool_calling/skills/news-weekly-summarizer/tech-news/docs/nvidia/developer/2026-10-27/3 Ways to Boost MoE Inference on NVIDIA DGX Spark.md