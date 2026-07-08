# NVIDIA Vera CPU Boosts AI Factory Throughput to Accelerate Agentic Workloads

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-07-07
- **原文連結**: https://developer.nvidia.com/blog/nvidia-vera-cpu-boosts-ai-factory-throughput-to-accelerate-agentic-workloads/

## 核心主題
NVIDIA Vera CPU 透過單核心性能提升 1.8 倍、降低延遲 40% 及增加記憶體頻寬，顯著提升 AI 工廠在代理工作負載下的效能與吞吐量。

## 關鍵重點
- **單核心性能大幅提升**：Vera CPU 採用 Olympus 核心架構，在滿載 Socket 下單核心性能比基準 CPU 快 1.8 倍，直接改善 RL 訓練的訓練循環、策略梯度品質及環境滾動完成率。
- **單片設計架構優勢**：採用單一計算晶片（monolithic compute die）整合 88 個 Olympus 核心、統一快取與可擴展一致性布線，避免多晶片設計中的跨晶片延遲問題，峰值負載延遲降低 40%。
- **記憶體頻寬與功耗優化**：配備 LPDDR5x 記憶體，提供高達 1.2 TB/s 總記憶體頻寬（每核心達 14 GB/s），為傳統 x86 資料中心 CPU 的 3 倍以上，同時功耗低於一半，大幅提升代理推理與互動式部署的響應速度。

## 結論
Vera CPU 不再只是背景基礎設施，而是直接驅動 AI 工廠吞吐量、響應速度與 GPU 效率的關鍵元件。透過減少停機時間、限制重計算並優化資料移動，Vera CPU 使整個系統在負載下保持高生產力，確保服務等級協議（SLA）的遵守。

---