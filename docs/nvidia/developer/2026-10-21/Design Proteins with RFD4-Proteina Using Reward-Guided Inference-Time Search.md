# Design Proteins with RFD4-Proteina Using Reward-Guided Inference-Time Search

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-10-21
- **原文連結**: https://developer.nvidia.com/blog/design-proteins-with-rfd4-proteina-using-reward-guided-inference-time-search/

## 核心主題
RFD4-Proteina 是一個結合獎勵導致的推理時間搜索的蛋白質設計模型，能夠同時設計蛋白質序列與全原子結構，大幅加速蛋白質設計流程。

## 關鍵重點
- 使用獎勵導致的推理時間搜索，將採樣步驟從約 400 步減少至 60 步，比 RFD3 快 3.8 倍
- 整合 CUDA 加速預言器（OpenFold3、TMol）進行推理時間搜索
- 支援 PD-L1 結合劑設計等任務，可接受標註 CIF 或條件規格
- 提供兩種使用方式：開源模型（適合訓練和開發）與 NIM 微服務（適合快速推理部署）
- 整合 rfd4-proteina-campaign 和 rfd4-proteina-package 技能，協調生成、搜索與評估流程
- 在 200 殘基時峰值記憶體減少 84%，BioIR 後端可加速 1.37-1.73 倍

## 結論
RFD4-Proteina 通過獎勵導致的推理時間搜索和高效的模型架構，顯著加速了蛋白質設計和藥物發現流程，為計算生物學家和藥物發現研究者提供了強大的工具。
---