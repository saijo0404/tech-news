# Introducing Z4M: storage-optimized compute for AI/ML and parallel file systems

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-07
- **原文連結**: https://cloud.google.com/blog/products/compute/storage-optimized-z4m-machine-series-are-ga/

## 核心主題
Google Cloud 正式推出新一代 Z4M 儲存優化型計算機系列，專為 AI/ML 訓練和推論工作負載設計，提供超大容量本地 SSD 儲存與高效能網路。

## 關鍵重點
- **超大儲存容量**：提供高達 168,000 GiB 的本地 SSD (LSSD) 儲存，搭配 400 Gbps 的 Cloud RDMA 網路，支援高達 192 vCPU 和 1,536 GiB 記憶體。
- **顯著效能提升**：相比 Z3 系列，儲存效能和吞吐量分別提升 70% 和 110%，支援 GPUDirect Storage 和 TPUDirect Storage，降低資料存取延遲達 60%。
- **靈活部署選項**：提供 VM 和裸金屬實例兩種選擇，裸金屬實例適合代理 AI 工作負載和特定授權需求，VM 則提供高 vCPU:LSSD 比例 (1:875)。
- **多工作負載支援**：適用於 AI/ML 訓練推論、並行檔案系統 (Weka/Sycomp/Silk)、企業級資料庫等場景，並支援 Hyperdisk 儲存類型。
- **客戶驗證**：Nutanix、Silk、Sycomp、WEKA 等合作夥伴驗證 Z4M 在 AI 工作負載上的卓越效能，讀取吞吐量提升約 2 倍，IOPS 提升達 79%。

## 結論
Z4M 系列為 AI/ML 和並行檔案系統工作負載提供高儲存容量、低延遲和高效能的解決方案，可大幅提升 GPU/TPU 利用率並優化雲端投資，是處理大規模資料處理任務的理想選擇。
---
