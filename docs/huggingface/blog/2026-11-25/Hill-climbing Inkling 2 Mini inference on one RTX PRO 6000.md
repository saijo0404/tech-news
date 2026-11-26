# Hill-climbing Inkling 2 Mini inference on one RTX PRO 6000

- **來源**: Hugging Face Blog
- **發布日期**: 2026-11-25
- **原文連結**: https://huggingface.co/blog/inkling-2-mini-inference-hillclimb

## 核心主題
這篇文章記錄了使用 vLLM + DSpark 在單卡 NVIDIA RTX PRO 6000 上優化 Inkling 2 Mini 推理性能的成功經驗，通過系統化實驗實現了 40% 的速度提升。

## 關鍵重點
- 使用 vLLM nightly + DSpark speculative decoding（7 drafts，probabilistic sampling）在 RTX PRO 6000 上實現 190.6 tok/s 的單用戶解碼速度，比基準快 40%
- 通過系統化實驗流程（控制→候選→控制）和嚴格基準測試，排除了多種不有效的配置，包括較短的 draft 長度、greedy 採樣等
- 最終部署的推理端點在網路延遲計入後達到 194.9 tok/s，達到硬體頻寬上限的 95%，並通過了長上下文針線檢索和並發測試

## 結論
這是一個可重複的優化範例，展示了如何系統化地使用 Hugging Face Jobs 和推理優化技能來提升模型推理性能，特別適合在 modest hardware 上部署高性能開源模型。
---
