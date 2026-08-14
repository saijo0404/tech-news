# Record train and deploy from one place with Strands Agents, LeRobot and Hugging Face Storage Buckets

- **來源**: Hugging Face Blog
- **發布日期**: 2026-08-13
- **原文連結**: https://huggingface.co/blog/amazon/strands-lerobot-streaming-data-loop

## 核心主題
這篇文章介紹了如何使用 Strands Agents、LeRobot 和 Hugging Face Storage Buckets 實現機器人數據記錄、訓練和部署的自動化循環。

## 關鍵重點
- 整合 Strands Agents、LeRobot 與 Hugging Face Storage Buckets，實現「記錄→訓練→部署」的自動化循環
- 使用流式數據讀取，無需下載完整資料集即可直接從 Hub 串流訓練
- 支援 Xet 儲存系統，內容定義區塊化與字節級去重，上傳效率提升約 4 倍
- 支援 SO-101 機器人、LeRobot 相容硬體及 NVIDIA GPU 訓練
- 訓練後的檢查點可直接部署到物理機器人，支援 LeRobot、GR00T、Cosmos3 等多個策略提供者
- 具備安全考量：限制提示注入風險、訓練數據信任邊界管理、使用 trusted orgs 和 safetensors 格式

## 結論
這是一個完整的機器人學習自動化管道，從數據錄製到訓練再到部署，所有步驟都可以在一個地方完成，大幅簡化開發流程並提升效率。
---
