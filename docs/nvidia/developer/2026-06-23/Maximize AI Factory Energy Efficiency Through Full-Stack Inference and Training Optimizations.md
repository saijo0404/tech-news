# Maximize AI Factory Energy Efficiency Through Full-Stack Inference and Training Optimizations

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-23
- **原文連結**: https://developer.nvidia.com/blog/maximize-ai-factory-energy-efficiency-through-full-stack-inference-and-training-optimizations/

## 核心主題
電力佔據 AI 工廠營運成本（OpEx）高達 40%，NVIDIA 透過硬體、軟體與模型設計的全面堆疊協同優化，幫助運營商在固定電力預算下最大化「每瓦效能」，進而降低單 token 成本並提升營收。

## 關鍵重點
- **推論優化：從 MoE 架構到 NVFP4 與系統層節能**：推論驅動營收，提升每瓦推論吞吐量直接增加可售 token 數量。MoE（混合專家）模型因每次僅激活部分專家，比同等參數量的密集模型更具能源效率（如 DeepSeek-R1）。系統層面，GB200 NVL72 採用高密度直接液冷設計與機櫃內功率平滑技術，允許在相同電力預算內部署更多 GPU；DSX 平台則透過動態功率分配與先進技術（如功率轉向、NVIDIA Dynamo）釋放閒置功率。精煉度方面，NVFP4 等窄精度格式在維持與 FP8 等效準確率的前提下，提供更高吞吐量與更低能耗。
- **訓練能效：降低 GPU 閒置時間的協同調度**：大型模型訓練中，GPU 工作負載不均導致部分 GPU 提早完成後進入閒置，造成能源浪費。密西根大學 ML.ENERGY 團隊研究顯示，針對個別 GPU 調整處理速度——將更多工作的 GPU（關鍵路徑）以最大速度運行、減少工作的 GPU 刻意降速——可在保持端到端訓練時間不變下減少總能耗。NVIDIA 與 ML.ENERGY 合作將此概念整合至 Megatron-LM，透過細粒度內核與階段級能量分析、能量感知排程與 GPU 頻率/功率上限調整，實現約 25% 的能耗節省。
- **NVIDIA DSX 平台：從機櫃到電網的全棧能源感知運維**：DSX 提供涵蓋晶片、系統、基礎設施軟體、設施與數位雙生的統一架構，分為 DSX MaxLPS（工廠內部）與 DSX Flex（電網層級）。MaxLPS 包含 45°C 液冷（提升 PUE）、動態功率分配與內建 GPU 進階方法；Flex 則連接電網訊號與外部能源。透過將工作負載放置、排程與功率分配與最高效的運算與冷卻區域對齊，運營商可在基礎設施層級增益之上疊加工作負載層級優化，持續提升每瓦 token 產量。

## 結論
AI 工廠根本上受到電力限制，而每瓦效能直接決定 token 成本與獲利。透過推論層级的 MoE 與窄精度優化、訓練層级的 GPU 協同速度調度，以及 DSX 平台的動態功率分配與電網感知運維，NVIDIA 的全堆疊方法將受限電力轉化為競爭優勢——使優化後的 AI 工廠在目標互動性下可達未優化工廠 2.6 倍的每秒每兆瓦 token 產量，讓營運商在固定電力預算下最大化 token 產出與營收。

---
