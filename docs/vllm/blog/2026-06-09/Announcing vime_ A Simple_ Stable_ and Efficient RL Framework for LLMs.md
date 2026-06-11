---
# Announcing vime: A Simple, Stable, and Efficient RL Framework for LLMs

- **來源**: vLLM Blog
- **發布日期**: 2026-06-09
- **原文連結**: https://vllm.ai/blog/2026-06-09-announcing-vime

## 核心主題
vLLM 社群發布 vime——一款結合 slime 強化學習訓練設計與 vLLM 推論優勢的 LLM 後訓練框架，將 Megatron 訓練迴圈與 vLLM rollout 串接為統一的 RL 管線，提供簡單、穩定且高效的強化學習微調體驗。

## 關鍵重點
- **解耦式 train-inference 架構**：vime 沿用 slime 的三階段設計（Megatron 訓練、vLLM + Router rollout 抽樣、資料緩衝區橋接），以 vLLM 取代原有 rollout 後端，確保訓練與推論在統一架構下運作，透過 `--vllm-` 前綴即可傳遞 vLLM 參數。
- **穩定訓練-推論對齊**：在 Qwen3-4B on A100 的 GRPO 實驗中，vime 的 `train_rollout_logprob_abs_diff` 穩定維持在 0.011 左右，而同框架基線則持續漂移至 0.77；對於 Qwen3-30B-A3B MoE 模型，新增的 R3（routing replay）機制將 logprob 差異從 0.019 進一步降至 0.013。
- **多硬體支援與效能驗證**：在 GB200 上 Qwen3-30B-A3B 的端到端 step 速度為 H200 的 1.72 倍（約 147 秒 vs 252 秒）；支援 Dense 與 MoE 模型、GRPO 與 PPO 演算法，並涵蓋 Qwen3 與 GLM-4.5 等模型，以 Apache 2.0 授權開源。

## 結論
vime 將 slime 的輕量高效訓練理念與 vLLM 的推論能力結合，為強化學習後訓練提供一條「簡單、穩定、高效」的主管線；未來將持續深化 vLLM 整合（Router、PD 分離、FP8）、擴展多硬體後端，並支援非同步管線與 Agentic RL 等新演算法。

---
