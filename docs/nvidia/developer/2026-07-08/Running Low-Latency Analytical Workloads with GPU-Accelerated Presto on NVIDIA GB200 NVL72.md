# Running Low-Latency Analytical Workloads with GPU-Accelerated Presto on NVIDIA GB200 NVL72

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-07-08
- **原文連結**: https://developer.nvidia.com/blog/running-low-latency-analytical-workloads-with-gpu-accelerated-presto-on-nvidia-gb200-nvl72/

## 核心主題
這篇文章介紹了使用 NVIDIA GPU 加速的 Presto 引擎在分析型工作載荷上的低延遲表現，特別是在 NVIDIA GB200 NVL72 集群上的優化結果。

## 關鍵重點
- GPU 加速的 Presto 在 TPC-H 分析基準測試中比多節點 CPU 集群快 2.5-8 倍，具體取決於活躍 GPU 數量與資料集大小
- 使用 NVIDIA cuDF 進行查詢執行、NVLink 實現 GPU 間高速通訊、以及 GPUDirect Storage (GDS) 實現從儲存設備到 GPU 記憶體的直接高速資料傳輸
- 在 GB200 NVL72 集群上，通過增加 I/O 任務大小、使用更多 I/O 線程以及重新撰寫查詢等優化措施，查詢運行時間可提升 64%
- GDS 讀取比 POSIX 讀取快約 2 倍，因為它繞過緩存並直接在 GPU 記憶體中使用 RDMA，減少 CPU 參與和 NUMA 邊界穿越延遲

## 結論
GPU 加速的 Presto 為分析型工作載荷提供低延遲和高吞吐量，已整合到 IBM watsonx.data 平台，可立即在生產工作負載上測試。

---
