# Lower the Cost of Building and Running Visual AI Agents with NVIDIA VSS Blueprint 3.3

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-09-29
- **原文連結**: https://developer.nvidia.com/blog/lower-the-cost-of-building-and-running-visual-ai-agents-with-nvidia-vss-blueprint-3-3/

## 核心主題
NVIDIA VSS Blueprint 3.3 透過 Build Vision Agent 技能和 Adaptive EVS 技術，大幅降低視覺 AI 代理的開發與運行成本，使開發者能從單一提示詞快速構建可部署的視覺 AI 系統。

## 關鍵重點
- **Build Vision Agent 技能**：從單一提示詞構建多工作流部署，基於四個驗證開發者檔案（base、alerts、lvs、search）組建最小化差異，自動合併共享基礎設施（Kafka、Redis、Elasticsearch）
- **瓶裝線演示**：在兩張 GPU RTX PRO 6000 Blackwell 主機上，30 分鐘內完成可預覽部署，包含搜尋、警報驗證和輪班報告，FP8 Cosmos 3 Nano 共享檢測器 GPU
- **Adaptive EVS 技術**：動態剪枝未變化的視覺區塊，警報情境化延遲降低 17%，並行實時 VLM 流增加 46%，60 分鐘影片摘要時間減少一半且 VLM 輸入 token 減少 80%
- **開發成本降低**：避免重複基礎設施，自動生成部署計畫並進行驗證，減少開發時間從數週縮短至 30 分鐘

## 結論
VSS 3.3 透過開發側的快速應用組建和運行側的 VLM 處理成本降低，解決視覺 AI 代理的三大成本驅動因素（開發成本、運行成本、變更成本），為生產級視覺 AI 代理提供可維護、高效率的解決方案。

---