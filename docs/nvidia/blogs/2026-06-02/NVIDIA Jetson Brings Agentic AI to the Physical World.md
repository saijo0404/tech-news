# NVIDIA Jetson 將代理式 AI 帶入實體世界

- **來源**: NVIDIA Blog
- **發布日期**: 2026-06-02
- **原文連結**: https://blogs.nvidia.com/blog/jetson-agentic-ai-physical-world/

## 核心主題
NVIDIA 發布 JetPack 7.2 並引入 NemoClaw 代理式 AI 框架至 Jetson 生產級平台，將代理式 AI 從伺服器與工作站延伸至機器人、工業自動化與邊緣裝置等實體世界應用，打造記憶體最佳化的邊緣代理部署基礎。

## 關鍵重點
- **JetPack 7.2 三大核心升級**：基於 Yocto 的 OS 支援提供輕量、可高度客製化的 Linux 基礎，適合記憶體受限的邊緣部署；CUDA 13 帶入 Jetson Orin 現有裝置；Jetson Thor 支援 MIG 與即時核心，開發者可保留專屬 GPU 資源給無法暫停的確定性工作負載（如機器人感知系統），Jetson AGX Orin 32GB 效能亦提升 20% 至 241 TOPS。
- **NemoClaw 與代理技能層加速開發**：NemoClaw 以單一指令部署至 Jetson，搭配 Linux 客製化、記憶體最佳化、模型基準測試等代理技能層，將原本需數週的開發任務縮短至數天；Metropolis VSS 藍圖技能更提供視覺推理代理，能觀察、解釋並對視覺訊號採取行動。
- **跨產業落地部署成果**：Solomon 的人型機器人以 NemoClaw 統整推理、感知、感測器融合、移動與操作；Advantech 在自家工廠部署代理式工廠大腦；Solomon、Hexagon Robotics 將 Thor 整合於人型機器人；Solomon 的主动感知技術與 Adva 的自動化決策驅動下一代工業營運；SandStar 以 NemoClaw 優化 40% 記憶體需求，從 16GB 降為 8GB 裝置降低成本；NoTraffic 優化 CUDA -library 降低 29% 記憶體；Hexagon、Zipline、1X、Universal Robots 等已規劃或進行 Yocto 基礎之 JetPack 7.2 生產部署。

## 結論
Jetson 平台以 JetPack 7.2 與 NemoClaw 的整合，標誌著代理式 AI 從資料中心走向實體世界的關鍵里程碑，零售店、人型機器人、智慧交通系統均已開始運行，物理 AI 代理的時代正式展開。
