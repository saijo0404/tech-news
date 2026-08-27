# How to Train a Cross-Embodiment Robot Navigation Policy with AI Agents

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-08-26
- **原文連結**: https://developer.nvidia.com/blog/how-to-train-a-cross-embodiment-robot-navigation-policy-with-ai-agents/

## 核心主題
本文介紹 NVIDIA COMPASS 框架，透過殘差強化學習（Residual RL）將預訓練的 X-Mobility 策略適配至特定機器人與環境。

## 關鍵重點
- **訓練架構**：以 Boston Dynamics Spot 四足機器人為參考，使用三種場景來源（內建倉庫、SAGE-10K 生成場景、Omniverse NuRec 重建環境）進行訓練
- **五階段工作流程**：環境驗證→場景準備→殘差訓練→評估→部署，每個階段都有明確的品質控制標準
- **硬體需求**：Ubuntu 22/24.04、32GB RAM、RTX GPU（建議 RTX 4080，16GB VRAM）、Isaac Sim 6.0
- **評估指標**：使用 COMPASS 指標評估目標到達率、跌倒率、移動時間等關鍵性能
- **cuVSLAM 集成**：提供部署時里程計，支援 GPS 受限環境的狀態估計
- **人類批准閘門**：確保品質控制，可將多個專家策略精煉為跨實體策略

## 結論
COMPASS 框架提供了一套完整的機器人導航策略訓練流程，從環境驗證到部署，強調品質控制與可擴展性。透過殘差強化學習，可以將預訓練策略適配至新機器人，並使用 COMPASS 指標進行嚴格評估，確保訓練品質。

---