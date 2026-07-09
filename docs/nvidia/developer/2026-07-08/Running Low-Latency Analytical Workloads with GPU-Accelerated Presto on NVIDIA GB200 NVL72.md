# Running Low-Latency Analytical Workloads with GPU-Accelerated Presto on NVIDIA GB200 NVL72

- **來源**: developer.nvidia.com/blog
- **發布日期**: 2026-07-08
- **原文連結**: https://developer.nvidia.com/blog/running-low-latency-analytical-workloads-with-gpu-accelerated-presto-on-nvidia-gb200-nvl72/

## 核心主題
這篇文章介紹了如何在 NVIDIA GB200 NVL72 集群上使用 GPU 加速的 Presto 引擎執行低延遲的分析工作負載，相比傳統 CPU 集群實現顯著的性能提升。

## 關鍵重點
- GPU 加速 Presto 在 NVIDIA DGX B200 和 GB200 NVL72 上相比多節點 CPU 集群，TPC-H 分析基準測試中延遲降低達 2.5-8 倍
- 關鍵技術包括 cuDF 查詢執行、NVLink GPU 間高速通訊，以及 GPUDirect Storage (GDS) 實現儲存裝置到 GPU 記憶體直接傳輸
- 集群優化措施包括增加 I/O 任務大小、使用更多 I/O 線程、重新編寫查詢以優化 GPU 利用率，整體 I/O 和通訊優化帶來 64% 更快的查詢執行時間

## 結論
透過 GPU 加速 Presto 與 NVIDIA GB200 NVL72 集群的整合，分析工作負載獲得低延遲和高吞吐量，特別適合需要快速迭代和互動儀表板的分析場景。

---
