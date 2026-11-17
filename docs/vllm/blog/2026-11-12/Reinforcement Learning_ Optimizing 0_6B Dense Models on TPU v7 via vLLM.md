# Reinforcement Learning: Optimizing 0.6B Dense Models on TPU v7 via vLLM

- **來源**: vLLM
- **發布日期**: 2026-11-12
- **原文連結**: https://vllm.ai/blog/2026-11-12-rl-small-dense-tpu-v7

## 核心主題
在 Google Cloud TPU v7 上優化小模型強化學習，將完整 rollout-to-update 週期從約 100 分鐘大幅縮短至 56 秒，實現 183K tokens/s 的吞吐量。

## 關鍵重點
- **性能提升**：解碼吞吐量從約 4K 提升至 ~183K tokens/s（提升 46 倍），端到端週期時間從約 100 分鐘降至 56 秒（速度快 107 倍）
- **優化策略**：跨堆疊協同設計，整合 vLLM、Tunix、MaxText、Pallas 等開源 TPU 工具，採用 TP1×DP128 架構（128 個獨立 vLLM 引擎）
- **主要挑戰**：小模型 RL 中，解碼排程、同步機制、注意力幾何、KV 緩存生命週期成為首要瓶頸，通過三階段優化解決
- **優化階段**：Phase I 配置調優（30K tokens/s）→ Phase II 跨堆疊解碼協同設計（130.5K tokens/s）→ Phase III 完整週期優化（183K tokens/s）
- **未採用的優化**：權重/KV 量化（INT8/FP8）、共享前綴級聯注意力、更大訓練微批次、更短回應上限均無明顯收益

## 結論
小模型 RL 是協調敏感型工作負載，需要硬體-軟體-模型協同設計。56 秒結果可在原始 0.6B 檢查點上運行 RL，無需 SFT 暖啟動。後續計劃包括多階段 SFT+RL 擴展、自動調優 Pallas RPA v3 和 Splash Attention 策略。

---