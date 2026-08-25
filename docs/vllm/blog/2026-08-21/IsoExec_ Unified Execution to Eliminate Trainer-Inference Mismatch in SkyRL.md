# IsoExec: Unified Execution to Eliminate Trainer-Inference Mismatch in SkyRL

- **來源**: vLLM Blog
- **發布日期**: 2026-08-21
- **原文連結**: https://vllm.ai/blog/2026-08-21-isoexec

## 核心主題
這篇文章介紹了 IsoExec，一個用於消除 RL 訓練和推理引擎之間浮點數不一致問題的統一執行抽象，並將其實現於 SkyRL 框架中。

## 關鍵重點
- **統一執行合約**: 建立跨訓練和推理的單一數值執行合約，確保浮點數舍入一致，實現零合約覆蓋的不一致
- **平行不變核**: 在張量、專家和序列平行化配置下保持數值一致性
- **分塊並行迴歸 GDN**: 設計 CPR 算法，在訓練、prefill 和 decode 階段之間保持一致的舍入計劃，同時保持高吞吐量

## 結論
實驗顯示，在 Qwen3.5-35B-A3B 模型的同步 RL 訓練中，IsoExec 將平均 logprob 差異降低至 0.0001 以下，但帶來了 25% 的端到端開銷。這表明消除訓練 - 推理不一致性可以穩定 RL 訓練，但需要權衡性能開銷。
---
