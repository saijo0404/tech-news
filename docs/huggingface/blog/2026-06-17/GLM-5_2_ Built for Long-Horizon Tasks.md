---
# GLM-5.2: Built for Long-Horizon Tasks

- **來源**: HuggingFace Blog (Z.AI)
- **發布日期**: 2026-06-17
- **原文連結**: https://huggingface.co/blog/zai-org/glm-52-blog

## 核心主題
智源（Z.AI）推出全新旗艦模型 GLM-5.2，以 MIT 開源授權提供 753B 參數與穩定 1M token 上下文，專為長程編碼與規劃任務設計，在多個基準中成為排名最高的開源模型。

## 關鍵重點
- **架構創新與推理最佳化**：提出 IndexShare 技術，讓每四個稀疏注意力層共用輕量索引器，在 1M 上下文下降低 2.9 倍每 token FLOPs；改進 MTP 層結合 KVShare、拒絕採樣與 TV 損失訓練，推測解碼接受長度提升 20%；推理引擎透過細粒度記憶體管理提升長上下文吞吐量。
- **強化學習與反作弊機制**：採用 slime 基礎設施將超過十個專家模型在兩天內合併，引入基於批評者的 PPO formulation 處理變長軌跡，並建立兩階段反作弊模組（規則過濾 + LLM 判讀）防止 Agent 操縱獎勵信號。
- **多管道部署與卓越基準表現**：模型權重已在 HuggingFace 與 ModelScope 公開，支援 transformers、vLLM、SGLang 等框架；引入 Effort Level 控制平衡效能與成本。在 FrontierSWE、PostTrainBench、Terminal-Bench 2.1 等基準中均為開源模型第一，Terminal-Bench 2.1 達 81.0 分（前代 GLM-5.1 僅 63.5）。

## 結論
GLM-5.2 將 1M token 上下文從論文指標轉化為實用的工程基礎——透過架構突破、嚴謹的反作弊訓練與開放部署管道，為開源編碼 Agent 與長程任務提供了 Opus 等級的性能表現。

---
