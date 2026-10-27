# How to Read Data into GPU Memory in Python with NVIDIA GPUDirect Storage

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-10-22
- **原文連結**: https://developer.nvidia.com/blog/how-to-read-data-into-gpu-memory-in-python-with-nvidia-gpudirect-storage/

## 核心主題
這篇文章介紹如何使用 NVIDIA KvikIO Python API 來讀取資料到 GPU 記憶體，並驗證是否使用了加速的 GPUDirect Storage (GDS) 路徑。

## 關鍵重點
- NVIDIA KvikIO 提供高階 Python 和 C++ 介面，位於 cuFile C API 之上，可加速檔案 I/O 到 GPU 記憶體
- KvikIO 和 cuFile 有獨立的路徑選擇機制：KvikIO 決定是否呼叫 cuFile，cuFile 則決定使用加速的 nvidia-fs 路徑還是 CPU 階段的相容路徑
- 可透過 CUFILE_STATS_LEVEL=3 和 gds_stats 工具檢查 cuFile 統計資訊，確認操作是否使用了加速路徑（nvfs 計數器）或相容路徑（posix 計數器）
- KvikIO 是 NVIDIA CUDA-X 資料科學套件的一部分，已用於 cuDF、cuCIM、cuPhoton 和 GPU 加速 Presto 等工作負載

## 結論
透過配置 KvikIO 和 cuFile 的運行時設定，開發者可以優化資料傳輸路徑，提升 AI 工作負載的效能。

---