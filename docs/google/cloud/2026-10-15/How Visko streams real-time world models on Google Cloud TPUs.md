# How Visko streams real-time world models on Google Cloud TPUs

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-16
- **原文連結**: https://cloud.google.com/blog/products/media-entertainment/how-visko-streams-real-time-world-models-on-google-cloud-tpus/

## 核心主題
AI 起點 Visko 與 Google Cloud 合作，在 30 天內成功將互動式世界模型 Orbis 部署到 Google Cloud TPU，實現實時視頻生成與同步音頻輸出。

## 關鍵重點
- **實時世界模型挑戰**：與離線視頻生成不同，實時世界模型必須嚴格遵守實時時鐘，每一幀視頻和音頻都必須在播放速度內完成渲染，否則世界會凍結。
- **單一 TPU 切片架構**：Visko 將完整的多模態管道（視頻擴散模型、超解析上轉換、音頻生成）部署在單一 Cloud TPU 切片上，使用 BF16 精度運行。
- **三項關鍵優化**：
  1. **Ulysses 上下文並行**：在 batch size 為 1 的情況下，通過所有到所有互連交換將 token 序列分佈到 TPU 芯片上
  2. **自訂 Pallas splash 注意力**：從 MaxDiffusion 集成自訂核，將注意力計算壓縮到片上 VMEM
  3. **音頻模型優化**：將音頻生成從 torchax 改為純 JAX，實現 5.8 倍速度提升
- **30 天快速部署**：從初始啟動到生產交接僅用 30 天，最終實現 1.07 倍播放速度的渲染。

## 結論
此案例展示了 AI 起點如何與 Google Cloud TPU 工程師緊密合作，在極短時間內將原型轉化為可生產的實時系統。對於其他構建超低延遲生成式 AI 的起點來說，這是一個寶貴的技術參考，特別是在處理實時視頻、世界模型和多模態推理方面的經驗。
---
