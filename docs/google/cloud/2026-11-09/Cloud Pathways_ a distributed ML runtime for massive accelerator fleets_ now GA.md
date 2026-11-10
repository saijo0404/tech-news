# Cloud Pathways, a distributed ML runtime for massive accelerator fleets, now GA

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-10
- **原文連結**: https://cloud.google.com/blog/topics/ai-infrastructure/cloud-pathways-a-distributed-ml-runtime-is-ga/

## 核心主題
Google Cloud 正式推出 Cloud Pathways，這是 Google DeepMind 開發的分佈式機器學習運算平台，現在在 GKE 上一般化可用，可支援大量異質加速器集群。

## 關鍵重點
- **單一控制器架構**：取代傳統多控制器管理，單一 JAX 客戶端過程可管理多個 TPU 切片，簡化跨切片資源管理
- **彈性訓練功能**：使用主機記憶體快照，在硬體故障時動態重新分佈訓練工作，確保訓練任務不會因單一切片故障而失敗
- **已驗證的企業採用**：超過 1.3 億個 Cloud TPU 芯片小時已被使用，包括 ZenteiQ 等客戶在科學基礎模型訓練上的成功應用
- **支援多種 TPU 世代**：支援 TPU v5e, v5p, Trillium (v6e), Ironwood (TPU 7x) 等硬體，並提供 Slurm 集群預覽整合

## 結論
Cloud Pathways 現在是 Google Cloud AI Hypercomputer 的核心組件，為企業提供訓練和服務大型 AI 工作loads 的可靠基礎設施，特別適合處理大規模、異質化的加速器集群場景。
---
