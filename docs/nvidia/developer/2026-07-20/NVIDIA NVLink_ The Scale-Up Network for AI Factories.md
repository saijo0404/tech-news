# NVIDIA NVLink: The Scale-Up Network for AI Factories

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-07-20
- **原文連結**: https://developer.nvidia.com/blog/nvidia-nvlink-the-scale-up-network-for-ai-factories/

## 核心主題
第六代 NVIDIA NVLink 提供專為 AI 工廠設計的超高頻寬、低延遲的 scale-up 網路，支援高達 3.6 TB/s 每 GPU 的頻寬和 260 TB/s 的機架級頻寬，在大型 MoE 和 LLM 工作負載中顯著超越商用以太網解決方案。

## 關鍵重點
- **超高頻寬與低延遲**：第六代 NVLink 提供 3.6 TB/s 每 GPU 的雙向 GPU 到 GPU 頻寬，端到端延遲比商用以太網解決方案低 3 倍，封包率高 10 倍，並提供 130 TFLOPS 的網路內計算能力。
- **極致協同設計**：NVLink 採用硬體與軟體（包括 NVIDIA Dynamo、TensorRT-LLM、NCCL 和 NIXL）跨層面的極致協同設計，支援分散式推理、專家並行和動態資源分配。
- **50 倍效能提升**：從 NVIDIA Hopper 到 NVIDIA Blackwell 的過渡中，實現了每瓦特 token 性能提升 50 倍，大幅優化 AI 工廠的 ROI。
- **堅韌性與運營功能**：具備控制平面韌性、可熱插拔交換器托盤、動態路由、服務中更新和細粒度遥測等特性，確保 AI 工廠的持續運行。
- **未來擴展性**：支援 NVLink-C2C 用於 CPU-GPU 一致性，以及 NVLink Fusion 用於自訂 XPU 的無縫整合，確保長期可擴展性。

## 結論
NVLink 是現代 AI 基礎設施的基石，透過極致協同設計和 proven 的技術堆疊，為 AI 工廠提供領先的性能、韌性、成熟度和持續創新，確保在 AI 加速時代中獲得可持續、可靠的投資回報。

---

*註：AI 生成內容可能不完全準確，重要資訊請自行驗證。*
