# How to Optimize NVFP4 Attention on NVIDIA RTX Blackwell Through Register Recycling

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-11-25
- **原文連結**: https://developer.nvidia.com/blog/how-to-optimize-nvfp4-attention-on-nvidia-rtx-blackwell-through-register-recycling/

## 核心主題
本文介紹如何在 NVIDIA RTX Blackwell GPU（SM120 架構）上透過 Register Recycling 技術優化 NVFP4 Attention 的效能，解決長序列推理中的計算瓶頸。

## 關鍵重點
- **NVFP4 優勢**：相比 BF16，NVFP4 提供更高的 Tensor Core 吞吐量，特別適合 RTX Blackwell 上的 Attention 工作負載。
- **SageAttention3 優化**：將每個 N128 score tile 分割成兩個 N64 register slots，在 Softmax 量化後重疊下一 tile 的 QK 計算與當前 tile 剩餘操作。
- **效能提升**：透過 Register Recycling 減少 Tensor Core 閒置時間，NVFP4 Attention 核延遲最高可提升 1.64 倍（Synthetic 8192 token causal 案例）。
- **實際應用**：Reactor 將此優化整合至生產環境，在 LongLive、Helios、OmniDreams 和 Cosmos 3 Nano 等世界模型工作負載上，端到端推論延遲降低達 15.34%。
- **開放源碼**：核心優化已合併至 FlashInfer main branch，開發者可複製分支並整合 SM120 NVFP4 Attention API 至支援的注意力層。

## 結論
透過巧妙的 Register Recycling 技術，NVIDIA 成功在 RTX Blackwell 工作站 GPU 上實現了比數據中心 GPU 更高的 Attention 效能，為視頻生成和世界模型推理提供了新的優化方向。此優化方案已開放源碼，可加速生態系統中的廣泛採用。

---