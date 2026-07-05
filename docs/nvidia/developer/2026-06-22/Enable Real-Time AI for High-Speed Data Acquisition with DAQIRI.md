# Enable Real-Time AI for High-Speed Data Acquisition with DAQIRI

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-22
- **原文連結**: https://developer.nvidia.com/blog/enable-real-time-ai-for-high-speed-data-acquisition-with-daqiri/

## 核心主題
NVIDIA 推出 DAQIRI（Data Acquisition for Integrated Real-time Instruments）——一種高性能網路程式庫，將硬體為中心的不彈性能資料取得架構轉向軟體定義、AI 啟用的邊緣運算模式，讓研究人員能即時處理高頻寬感測器與偵測器資料串流，無需等待資料儲存後再分析。

## 關鍵重點
- **從「先儲存再分析」到「串流即時處理」**：現代感測器與偵測器（如 LCLS-II 的 1 MHz 光子脈衝、工業 CT 掃描器）的資料產出率持續增長，傳統「collect → store → analyze」架構已成瓶頸。DAQIRI 將資料取得直接接入 NVIDIA 軟體生態系（Holoscan 即時多模態處理、TensorRT 即時推論、nvCOMP 串流壓縮），讓開發者能在串流中執行濾波、推論、壓縮、事件篩選與自适应控制，無需修改現有儀器。
- **零拷貝、低延遲的底層架構**：DAQIRI 基於 DPDK 繞過 Linux 核心，直接從 NIC 將資料路由至 GPU 的 DMA 緩衝區，實現零記憶體拷貝，延遲僅限 PCIe 傳輸時間。支援 100s of Gbps 線速處理（UDP 與 RoCE v2），具備自動封包重排、資料型別轉換、硬體流程引導、YAML 驅動配置與即插即用的 C++/Python API。
- **A-GHOST 專案應用案例**：CERN 的 HL-LHC 升級將亮度提升 10 倍，ATLAS 偵測器在線上系統中需拒絕超過 99% 的碰撞資料。A-GHOST 專案使用 DAQIRI 將 GPU 拉近原始偵測器資料，對被捨棄的串流應用更強大的 AI 搜尋（如卷積自編碼器、時間卷積神經網路與 transformer 模型），實現全串流的即時分析。YAML 配置範例展示了從 int4 壓縮 payload 轉換為 fp16 張量、批次化 1024 封包、跳過網路標頭等完整流程，應用端程式碼可精簡至數行。

## 結論
DAQIRI 代表了科學資料取得的範式轉移——將邊緣超級電腦（從 DGX Spark 到 RTX Pro Server）與 GPU 運算直接連接到高頻寬感測器，移除了「先儲存」的關鍵路徑依賴。研究人員不僅能獲得即時數據洞察，還可將精選的高品質資料傳輸至超級電腦進行更深層 AI 分析，讓從資料收集到發現的旅程大幅加速。

---
