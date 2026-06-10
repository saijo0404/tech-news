# 使用 NVIDIA JetPack 7.2 以記憶體效率在邊緣部署代理式 AI

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-02
- **原文連結**: https://developer.nvidia.com/blog/deploy-agentic-ready-ai-at-the-edge-with-memory-efficiency-in-nvidia-jetpack-7-2/

## 核心主題
NVIDIA JetPack 7.2 以單一指令部署 NemoClaw、引入代理技能層、官方 Yocto 支援與 Jetson Thor MIG 分割，讓開發者在記憶體受限的邊緣裝置上以更低總體擁有成本部署安全、可預測的代理式 AI 工作負載。

## 關鍵重點
- **NemoClaw 一鍵部署與代理技能自動化開發**：JetPack 7.2 預先配置 NemoClaw 相依性，執行單一命令即可在 Jetson 上運行代理式物理 AI；Jetson 代理技能涵蓋 Linux 客製化、記憶體最佳化與模型基準測試，將原本需數週的手動開發縮短至數天，並支援 DeepStream 與 Metropolis VSS 視覺管線建構。
- **Jetson Thor MIG 分割與 Yocto 官方支援**：MIG 將 Blackwell GPU 分割為兩個隔離實例（12 SM 大分割給推論與視覺、8 SM 小分割給機器人控制與安全關鍵工作負載），結合 Preemptible RT 核心實現確定性多工；Yocto Project 提供可客製、可複現的 Linux 分佈，搭配 Konsulko Group、Peridio、Balena、RidgeRun 等夥伴生態系加速產能部署。
- **統一軟體基礎與 Super Mode 效能提升**：JetPack 7.2 將 Jetson Thor 的 Ubuntu 24.04 + Kernel 6.8 + CUDA 13 堆疊向下延伸至 Orin 家族，實現單一軟體基礎；Jetson AGX Orin 32 GB 新增 Super Mode，GPU 時脈推升至 1.3 GHz、功耗上限至 60W，AI 運算由 200 TOPS 增至 241 TOPS（提升逾 20%），以 45% 成本獲得接近 64 GB 模組的表現，支援 Nemotron 3 Nano 30B 等生成式 AI 模型。

## 結論
JetPack 7.2 以軟體升級釋放既有 Jetson 硬體價值，將代理式 AI 從雲端延伸至記憶體受限的邊緣裝置，讓機器人以更低的 TCO 在工廠、機器人、智慧醫療等實體場景中可靠運行。
