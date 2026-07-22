# NVIDIA Vera CPU: Olympus Cores Built for Maximum Single-Thread Performance in Agentic AI

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-07-21
- **原文連結**: https://developer.nvidia.com/blog/inside-nvidia-vera-cpu-olympus-cores-built-for-maximum-single-threaded-performance-in-agentic-ai/

## 核心主題
NVIDIA Vera CPU 以 Olympus core 為核心，針對 Agentic AI 工作負載設計，透過最大化單線程性能、利用亂序執行與深度記憶體級並行度，加速不规则、分支密集且延遲敏感的軟體路徑。

## 關鍵重點
- **Olympus Core 架構**：整合優化分支預測器、關鍵路徑加速、複雜向量優化與延遲優化緩存子系統，專注於提升每週期指令數（IPC）以處理高併發 AI 基礎設施工作負載。
- **單線程性能優化**：針對 Agentic AI 工作負載特性，強調即使在完整 socket 負載下仍具備強勁的單線程性能，以確保每個代理步驟的持續進展。
- **NVIDIA Spatial Multithreading (SMT)**：採用資源更有效分割的 SMT 技術，將 Olympus core 設計為高吞吐量單線程核心，同時允許兄弟核心處理管理活動，減少干擾並提升可預測性。
- **Scalable Coherency Fabric (SCF)**：提供高達 3.4 TB/s 的片上頻寬與 164 MB 統一 L3 緩存，整合 Olympus cores、共享緩存、記憶體控制器、I/O 與 NVLink-C2C 介面，避免片上跳延遲。
- **SOCAMM2 LPDDR5X 記憶體**：提供高達 1.2 TB/s 的總頻寬（每核心達 14 GB/s），相比傳統 DDR5 設計具有更低的功耗與更高的 RAS 能力，並支援模組化記憶體更換。
- **安全與擴展性**：透過 NVLink-C2C、CXL 3.1、PCIe 6.4 與 Confidential Computing 實現安全、高頻寬資料傳輸，支援雙插槽擴展且每個插槽為單一 NUMA 領域。
- **性能表現**：根據 SPEC CPU® 2026 內部測試，在 Agentic AI 工作負載上最高達 1.8 倍性能提升。

## 結論
NVIDIA Vera CPU 透過 Olympus core 與周邊架構的協同優化，成功解決了 Agentic AI 工作負載對 CPU 性能的特殊需求，為 AI 工廠規模的應用提供了高單線程性能、可預測延遲與安全擴展的解決方案。

---