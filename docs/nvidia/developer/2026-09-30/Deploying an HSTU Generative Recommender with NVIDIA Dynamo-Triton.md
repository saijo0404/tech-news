# Deploying an HSTU Generative Recommender with NVIDIA Dynamo-Triton

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-09-30
- **原文連結**: https://developer.nvidia.com/blog/deploying-an-hstu-generative-recommender-with-nvidia-dynamo-triton/

## 核心主題
這篇文章介紹了如何使用 NVIDIA Dynamo-Triton、PyTorch AOTI 和 FlexKV 來部署 HSTU 生成式推薦系統，並展示了性能優化成果。

## 關鍵重點
- HSTU 生成式推薦系統將推薦問題重新表述為用戶行為的序列建模，將用戶互動、上下文、候選項目和行動視為高基数事件序列中的 token
- PyTorch AOTI（Ahead-of-Time Inductor）將 HSTU 排名模型提前編譯為原生 C++ 代碼，減少 Python 運行時開銷，並提供可部署的 artifacts
- FlexKV 支持的 KV 緩存可避免重新計算長用戶歷史中的重複計算，在 NVIDIA RTX PRO 6000 Blackwell GPU 上，八層 HSTU 模型在批次大小為 8 且 GPU KV 緩存命中率為 100% 的情況下，相比未緩存的相同 AOTI 配置，延遲降低了 5.93 倍

## 結論
這種部署工作流程為開發者提供了從 PyTorch 開發到生產推理的實用路徑，無需為不同運行時重新編寫模型。通過結合 Dynamo-Triton 生產服務、PyTorch AOTI 編譯 artifacts、NV Embedding Cache 降低 GPU 記憶體需求以及 FlexKV 減少重複計算，實現了低延遲的 HSTU 推薦模型服務。

---