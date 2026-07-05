# NVIDIA GTC Taipei at COMPUTEX: Live Updates on What's Next in AI

- **來源**: blogs
- **發布日期**: 2026-05-21
- **原文連結**: https://blogs.nvidia.com/blog/nvidia-gtc-taipei-computex-2026-news/
- **更新日期**: 2026-06-01

## 核心主題
Jensen Huang 於台北流行音樂中心發表 GTC Taipei 主旨演講，宣告「AI 已成為獲利與 GDP 的驅動者」。NVIDIA 全面轉向 Agentic AI 基礎設施，涵蓋 AI Factory 架構、Vera Rubin 量產、Agent Toolkit、個人代理電腦、實體 AI 等完整產品線。

## 關鍵重點

### AI Factories — 新基礎建設
- Jensen Huang 表示「AI 現在是獲利產生器、GDP 產生器」，Token 已成為有價值的收入單位
- NVIDIA DSX 架構：DSX MaxLPS 在同一功耗預算下提供 40% 更多 GPU，DSX OS 為開源可擴展
- 全球建設者（CoreWeave、Nebius、Nscale 等）正在打造「人類歷史上最大的基礎設施擴張」
- Huang 強調「運算即收入」：在 AI Factory 時代，效能/瓦特等於收入

### NVIDIA Vera Rubin 全面量產
- Vera Rubin 供應鏈規模是 Grace Blackwell 的兩倍，150 家台灣供應商、350+ 工廠、30 國參與
- 完整五機櫃平台：Vera Rubin NVL72、Vera CPU、Groq 3 LPX、Spectrum-6 SPX 乙太網路、Vera BlueField-4 STX
- **Spectrum-X Ethernet Photonics**：全球首款 200Gb/s SerDes 乙太網路交換器，搭載共封裝光學技術，CoreWeave、Lambda、Oracle 為首批採用者
- **NVIDIA Vera CPU**：專為 Agent 時代打造的 CPU，88 核心、1.2TB/s LPDDR5X 頻寬、3.6TB/s 片上互連，無晶片簇邊界
- **Vera BlueField-4 STX**：矽層級安全，DOCA Argus 威脅偵測從分鐘縮短至毫秒級

### Agent Toolkit — Agent 的執行環境
- **NVIDIA Agent Toolkit**：企業級完整堆疊運行時，整合 LLM、Agent Harness 與治理管理
- **Cadence-NVIDIA 晶片設計 Super Agent**：自動 orchestrating RTL 產生、測試矩陣、回歸測試與除錯，驗證速度提升 **40 倍以上**
- **Nemotron 3 Ultra**：550B MoE 模型，推論速度提升 **5 倍**，運行成本降低 **30%**，開源
- NVIDIA CUDA-X 函式庫（cuDF、cuOpt、AI-Q、NeMo、PhysicsNeMo、CUDA-Q）已開放給 Agent 調用
- **NVIDIA OpenShell**：安全的 Agent 執行環境，提供沙盒、集中策略執行與治理閘道

### 個人電腦重新發明 — RTX Spark
- **NVIDIA RTX Spark**：與 MediaTek 合作打造，Blackwell RTX GPU（6,144 CUDA 核心）+ 20 核心 Grace CPU，1 petaflop AI 效能
- 首批專為個人代理打造的 Windows 電腦：筆記型電腦、桌面個人代理機、**DGX Station for Windows**（桌面型 AI 超級電腦）
- Adobe 重新架構 Photoshop 與 Premiere 支援 RTX Spark，AI 與圖形效能提升 **2 倍**
- Huang 稱這是「40 年來首次全面產品線重新發明」

### 實體 AI — AI 進入物理世界
- **NVIDIA Cosmos 3**：世界基礎模型，採用 Mixture-of-Transformers 架構，可從任何視角理解與模擬物理世界，附完整開源工具鏈
- **NVIDIA DRIVE Hyperion**：結合 Halos OS 成為全球自動駕駛平台，涵蓋全球約 97% 的移動服務
- **Alpamayo 2 Super**：開源 AV 推理模型，支援端到端決策；搭配 AlpaGym 閉環強化學習框架與 OmniDreams 高擬真場景生成
- **Isaac GR00T Reference Humanoid Robot**：首個開放人形機器人參考設計，基於 Jetson Thor 與 Isaac GR00T 開發平台

### DGX Spark 更新
- **NemoClaw** 簡化安裝器，新增 Hermes Agent 與 OpenClaw 支援
- vLLM 推論效能提升最高 **2.6 倍**（Qwen3.6 35B），採用核最佳化、NVFP4 量化與多 Token 預測
- **Cluster Assistant**：可將 2-4 台 DGX Spark 組建多節點叢集

## 結論
Jensen Huang 將 NVIDIA 定位為「基礎設施公司」而非僅是 GPU 或系統公司。NVIDIA 建立了一套統一的 Agentic Computing 模式——模型 + Harness + Skills + Runtime，從雲端到邊緣、從 PC 到機器人皆可運行。Vera Rubin 已全面量產，Agent Toolkit 與 RTX Spark 個人代理電腦標誌著個人計算的重新發明，而 Cosmos 3 與 DRIVE Hyperion 則代表 AI 正式進入物理世界。
