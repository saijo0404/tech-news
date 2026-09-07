# Not All LLM Workloads Are Equal: Benchmarking TPU Performance on Classification vs. Generation

- **來源**: Google Cloud Blog Developers & Practitioners
- **發布日期**: 2026-09-05
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/not-all-llm-workloads-are-equal-benchmarking-tpu-performance-on-classification-vs-generation/

## 核心主題
這篇文章比較了 Gemma 3 12B 和 27B 模型在 Google Cloud TPU v6e 上的分類與生成任務性能差異，揭示不同工作負載對硬體壓力的影響。

## 關鍵重點
- **生成任務性能差異**：在高併發生成任務中，Gemma 3 12B 模型表現優異（128 用戶時達 8.19x 倍率），而 27B 模型僅達 4.12x 倍率，顯示大模型在高併發下易受記憶體或運算限制。
- **分類任務性能齊平**：在預填充-heavy 的分類任務中，12B 和 27B 模型表現相近（128 用戶時分別達 6.37x 和 6.04x 倍率），可安全部署大模型而不影響效能。
- **硬體飽和邊界**：應根據工作負載類型選擇模型——高併發生成任務建議使用 12B 模型，分類任務可放心使用 27B 模型，並透過調整 vLLM 參數（如 batched tokens、TPU bucket padding）避免資源浪費。

## 結論
透過針對不同工作負載類型進行模型選擇與參數優化，可避免硬體飽和、提升效能並降低成本。企業應根據實際需求（如分類或生成）右大小模型架構，並採用 GKE 與 TPU v6e 等基礎設施實現高效能擴展。

---