# Enabling Real-Time AI for Scientific Instruments with GPU-Native Data Acquisition

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-11-19
- **原文連結**: https://developer.nvidia.com/blog/enabling-real-time-ai-for-scientific-instruments-with-gpu-native-data-acquisition/

## 核心主題
NVIDIA DAQIRI 軟體庫透過將高頻寬儀器數據直接送入 GPU 記憶體，使科學儀器能在數據採集過程中即時處理與分析，並引入硬體封裝重排序、ibverbs 引擎與直接 polling 模式等最新功能。

## 關鍵重點
- **高動態範圍相機案例**：伯克利國家實驗室開發的高動態範圍電子顯微鏡相機，每秒產生超過 500 Gbps 數據，透過 FPGA 讀取電子與 DAQIRI 協作，實現即時數據處理。
- **DAQIRI 硬體封裝重排序**：支援 NVIDIA ConnectX-7 或更新網卡，將封裝重排序任務移至硬體層，減少延遲與記憶體負擔。
- **ibverbs 引擎效能提升**：相比 DPDK 引擎，ibverbs 引擎在小包尺寸下每核心吞吐量提升近一倍，支援超過 200 Gbps 極端數據速率。
- **直接 polling 模式降低延遲**：透過直接 polling 模式，應用線程可直接收發數據包，實現 2-4 微秒的極低延遲，適合對延遲敏感的即時反饋應用。

## 結論
透過 GPU 原生數據採集，科學儀器設計者可重新思考採集限制，將更多工程精力聚焦於測量品質與科學洞察，同時提升數據處理靈活性與即時性。

---