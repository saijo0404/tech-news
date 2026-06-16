---
# Fastest, Largest, Strongest: NVIDIA Blackwell Sweeps MLPerf Training 6.0

- **來源**: NVIDIA Blog
- **發布日期**: 2026-06-16
- **原文連結**: https://blogs.nvidia.com/blog/blackwell-mlperf-training-6-0/

## 核心主題
NVIDIA Blackwell 平台在 MLPerf Training v6.0 中蟬聯全項目冠軍，是唯一提交所有七項測試結果的平台，涵蓋從 512 顆至 8,192 顆 GPU 的超大規模訓練，並透過 GB300 NVL72 較 GB200 最高提升 1.6 倍效能展現 Blackwell Ultra 硬體優勢。

## 關鍵重點
- **效能與硬體升級**：GB300 NVL72 憑藉 NVFP4 低精度訓練、更高運算密度、擴展記憶體容量與電源預算，較 GB200 NVL72 最高達成 1.6 倍訓練加速。MLPerf 6.0 新增 DeepSeek-V3 671B 與 GPT-OSS-20B 兩項 MoE 預訓練工作負載，NVIDIA 平台在全部七項基準測試中皆創下最快速度。
- **8,192 GPU 極限規模與夥伴協作**：CoreWeave 以 GB300 NVL72 搭配 Spectrum-X 乙太網路在 8,192 顆 GPU 上於 2.02 分鐘完成 DeepSeek-V3 671B 訓練；Microsoft Azure 同樣以 8,192 顆 GB200 GPU 在 7.07 分鐘內達到 Llama 3.1 405B 參考品質目標。共 19 家生態圈夥伴參與提交，涵蓋 Google Cloud、HPE、Google Cloud 上的 Thinking Machines Lab 達 2 倍加速等案例。
- **生產級可靠性設計**：NVIDIA GPU 在出廠前經歷 30 多個製造測試階段預防故障，Reliability, Availability and Serviceability Engine 即時監控晶片並自動繞過異常節點。NVRx 復原延伸功能自動偵測效能低落節點，當故障發生時從最近的檢查點恢復而非重新訓練，Spectrum-X 乙太網路亦能在毫秒內重新路由故障鏈接。

## 結論
NVIDIA Blackwell 在 MLPerf Training 6.0 中展現的「最快、最大、最強」不僅是基準測試的勝利，更是從硬體設計、網路協同到軟體生態的全堆疊勝利。加上生產級可靠性保障，企業能自信地將訓練週期從數月縮短至數小時，加速將 AI 創新轉為商業價值。

---
