# VeRL-Omni v0.2.0: Faster Diffusion RL and Stable Omni Training

- **來源**: vLLM Blog
- **發布日期**: 2026-08-20
- **原文連結**: https://vllm.ai/blog/2026-08-20-verl-omni-v0-2-0

## 核心主題
VeRL-Omni v0.2.0 發布了兩個主要改進：更快的擴散 RL 訓練和更穩定的泛模態訓練，為生產級多模態強化學習奠定更堅實的基礎。

## 關鍵重點
- **更快的擴散 RL**：通過請求級別批處理，Qwen-Image FlowGRPO 的生成時間從 226 秒降至 108 秒，GPU 利用率提升至 100%，提升 52%
- **穩定的泛模態訓練**：引入 verl V1 訓練器和可重用的 Omni 模型適配器層，支持 Qwen3-Omni Thinker 等多個模型
- **MMK12 基準測試**：實現 0.998 的 actor-rollout Pearson 相關係數，驗證了多模態數據處理和一致性信號的有效性
- **擴展的模型支持**：新增 LTX2.3、Qwen-Image-Edit、BAGEL、SD3.5+DiNa-LRM 等模型和 Flow-DPPO 等演算法支援

## 結論
這次發布通過請求級別批處理和可重用的訓練架構，顯著提升了擴散模型的訓練效率，同時建立了更穩定的泛模態訓練基礎，為未來多模態 RL 的生產化應用提供了更強大的工具集。
---
