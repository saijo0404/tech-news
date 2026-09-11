# How Full-Stack NIM Optimizations Deliver 2.5x More Users on Nemotron 3 Ultra

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-09-10
- **原文連結**: https://developer.nvidia.com/blog/how-full-stack-nim-optimizations-deliver-2-5x-more-users-on-nemotron-3-ultra/

## 核心主題
NVIDIA 透過全棧 NIM 優化技術，在 4xB200 系統上實現比基準服務堆疊高 2.5 倍的系統吞吐量，大幅提升並發用戶容量。

## 關鍵重點
- NIM 2.0.12 優化服務堆疊結合了自動調優核、張量並行、前綴和狀態重用、調度器和記憶體優化，以及 MTP 猜測解碼，在 50 TPS/用戶目標下達到每秒 1,997 個 token。
- 在 50 TPS/用戶目標下，NIM 開啟的曲線比基準曲線提供超過 2.5 倍的系統吞吐量，直接轉化為相同互動性下的更多並發用戶。
- NIM 將模型和 GPU 感知的服務選擇打包成可部署的微服務，包含驗證過的配置、標準 API 和通過 NVIDIA AI Enterprise 的企业級容器生命週期。
- 開發者可以使用 NVIDIA AIPerf 重播代表性工作負載來比對 NIM，並選擇滿足延遲 SLO 的 Pareto 點。

## 結論
NVIDIA NIM 提供了經過驗證的性能工程和企業級容器生命週期，使組織能夠在實際的多用戶服務中實現更高的用戶容量，同時保持部署路徑的實用性。

---