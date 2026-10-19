# Day 0 support for Reflection's Beam on Google Cloud: 5x faster perf with llm-d and NVIDIA Dynamo

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-17
- **原文連結**: https://cloud.google.com/blog/topics/ai-infrastructure/day-0-support-with-5x-perf-for-reflection-beam-on-google-cloud/

## 核心主題
Google Cloud 宣布對 Reflection 的 Beam 模型提供 Day 0 支援，並透過 llm-d 和 NVIDIA Dynamo 優化服務堆疊，實現最高 5 倍效能提升和 8 倍延遲降低。

## 關鍵重點
- **Beam 模型特性**：Beam 是 500B 參數級別的高效推理模型，比可比開源模型有 3-4 倍更高的推理計算效率，特別適合軟體工程和長時程代理任務。
- **系統層面優化**：在 A4X Max 實例上實現最高 5 倍吞吐量提升和 8 倍延遲降低，在 G4 VM 上實現 2 倍吞吐量提升和 8 倍延遲降低。
- **高效多輪服務**：支援 KV cache 感知的路由、prefill/decode 分離、推測解碼和分層 KV cache 快取卸載，減少長編程會話中的重複提示重計算。
- **完整優化部署方案**：提供可在 AI-Hypercomputer/GPU recipes、llm-d 倉庫和 Gemini 平台 Model Garden 中快速部署的優化部署指南。

## 結論
透過結合模型層面（Beam 的 3-4 倍推理效率）與系統層面（AI Hypercomputer 優化服務）的雙重優化，開發者可以高效地部署和運行 Beam 模型，特別適合代理工作負載，並提供完整的開源部署工具和最佳實踐。
---

檔案已成功儲存至指定路徑。