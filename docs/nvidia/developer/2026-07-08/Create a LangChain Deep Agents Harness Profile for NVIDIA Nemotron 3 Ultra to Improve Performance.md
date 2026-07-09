# Create a LangChain Deep Agents Harness Profile for NVIDIA Nemotron 3 Ultra to Improve Performance

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-07-08
- **原文連結**: https://developer.nvidia.com/blog/create-a-langchain-deep-agents-harness-profile-for-nvidia-nemotron-3-ultra-to-improve-performance/

## 核心主題
本文介紹如何使用 harness engineering（Harness 工程）來優化 NVIDIA Nemotron 3 Ultra 模型在 LangChain Deep Agents 上的表現，而不需要微調（fine-tuning）。

## 關鍵重點
- 使用評估基準（evaluation benchmarks）和每模型自訂入口點（如 LangChain agent harness profiles）來優化代理系統
- 通過「評估→分析失敗→提出 harness profile 變更→驗證修復」的迭代循環來最小化退化和過度擬合
- 自動化透過代理提案者（如 LangSmith Engine 和 ralph loop）實現，確保解決方案可泛化而非過度擬合

## 結論
這種方法使開源模型能夠接近專有 frontier 模型的準確度，同時降低微調所需的專業知識與硬體成本。

---

檔案已成功儲存至指定路徑。