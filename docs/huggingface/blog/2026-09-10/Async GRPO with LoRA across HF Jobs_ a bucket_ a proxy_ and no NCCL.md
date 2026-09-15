# Async GRPO with LoRA across HF Jobs

- **來源**: Hugging Face Blog
- **發布日期**: 2026-09-10
- **原文連結**: https://huggingface.co/blog/asyncgrpo-lora-hfjobs

## 核心主題
這篇文章介紹了 AsyncGRPOTrainer 支援 LoRA adapter 訓練的架構，透過 Hugging Face Jobs 環境實現訓練與推理解耦，大幅提升訓練效率。

## 關鍵重點
- **架構設計**：訓練器 Job + 2 個 vLLM Job + 1 個 Proxy 伺服器，使用 Storage Bucket 作為共享文件系統（FUSE 掛載），無需完整模型同步
- **KV prefix router 優化**：基於 chained hashes 識別 prompt 並路由到持有 KV prefix 的副本，Affinity hit 達 84.5%
- **訓練速度提升 3.7-3.9 倍**：500 步驟訓練從 3 小時 27 分鐘縮減至 53 分鐘，MFU 從 3.9% 提升至 19-23%
- **Rank-1 LoRA adapter**：僅幾 MB 即可替代完整模型 3GB，支援 LoRA 廣播到所有 replica
- **Proxy 伺服器功能**：負責添加 HF Token 認證、路由 rollout 至持有 KV prefix 的副本、廣播 adapter 更新
- **實驗優化成果**：禁用 Gradient Checkpointing 後 MFU 達 23%，訓練樣本量增加 31%

## 結論
AsyncGRPO 與 LoRA 結合的架構在 Hugging Face Jobs 環境中展現了顯著的性能提升，特別適合分布式訓練場景。訓練與推理解耦的設計避免了 NCCL 跨節點通信的瓶頸，為大模型訓練提供了新的效率優化方向。
---
