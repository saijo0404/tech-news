# Beyond a Single Model: Building Mixture-of-Models Systems with vLLM Semantic Router

- **來源**: vLLM
- **發布日期**: 2026-07-21
- **原文連結**: https://vllm.ai/blog/2026-07-21-vllm-sr-new-chapter-mom

## 核心主題
這篇文章介紹了 vLLM Semantic Router 如何從單一模型路由演進為混合模型系統架構，透過整合多個專業化模型來解決單一模型無法適應所有場景的問題。

## 關鍵重點
- **Mixture-of-Models (MoM) 架構**：透過單一介面整合多個專業化模型，將分散的 AI 堆疊整合至單一模型邊界，使資源分配成為模型系統內部機制。
- **vLLM Semantic Router 發展歷程**：一年內累積 5,000 stars、150+ 貢獻者與 30 萬下載量，經歷 Iris、Athena、Themis 三個主要版本，從模型選擇演進為推理控制系統。
- **四大平面架構**：包含 Artifact（可移植模型組件）、Learning（學習與訓練）、Execution（執行與推理）、Physical（硬體與部署）。
- **推理時決策**：引擎在推理階段決定使用單一模型或調用多個模型，保持應用層面的簡單性，同時支援跨設備、環境和場景的完整智能系統。

## 結論
vLLM Semantic Router 正從智能路由向建構可運作的混合模型系統演進，目標是讓應用端只需呼叫單一模型身份，即可獲得跨硬體、跨環境的完整智能系統體驗。

---