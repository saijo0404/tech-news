# Why Performance per Watt Is the Ultimate Metric for AI Infrastructure Efficiency

- **來源**: NVIDIA Blog
- **發布日期**: 2026-07-14
- **原文連結**: https://blogs.nvidia.com/blog/performance-per-watt-ai-infrastructure-efficiency/

## 核心主題
這篇文章探討了為什麼「每瓦特效能」是 AI 基礎設施的關鍵指標，並介紹了 NVIDIA 如何透過全栈程式碼設計提升 AI 推理效能。

## 關鍵重點
- 每瓦特效能是 AI 基礎設施無法欺騙的指標，直接影響營收與利潤，因為 AI 工廠在固定電力預算下能產生的 token 數量決定了其盈利能力
- NVIDIA GB300 NVL72 平台相比 Hopper 世代提升達 25 倍每瓦特效能，透過從 8-GPU 到 72-GPU 領域架構的擴展實現
- 採用全栈程式碼設計，從矽電路到軟體層面全面優化，包括 NVLink Switch、推理軟體堆疊（Dynamo、TensorRT LLM 等）及 DSX MaxLPS 電力管理
- 實際生產環境驗證：Anthropic、OpenAI、SpaceXAI 等領先 AI 實驗室已採用 Blackwell NVL72 平台運行推理服務

## 結論
在電力受限的世界中，透過全栈程式碼設計與實際生產驗證，NVIDIA 持續提升 AI 基礎設施的每瓦特效能，幫助組織在電力預算下最大化收益並降低 token 成本。

---