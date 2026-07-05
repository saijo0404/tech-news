# NVIDIA Brings Trusted, 24/7 AI Agents to Telecom Operations

- **來源**: NVIDIA Blogs
- **發布日期**: 2026-06-23
- **原文連結**: https://blogs.nvidia.com/blog/telecom-ai-agents-dtw-ignite-2026/

## 核心主題
NVIDIA 與合作夥伴在 TM Forum DTW Ignite 2026 展示電信自主網路的三大支柱——合成數據、電信領域模型、安全 Agent 執行環境與加速模擬，協助電信營運商從「任務導向自動化」邁向「端到端自主營運」，讓 AI Agent 能全天候監控、預測問題並安全地協調網路、IT 與業務系統的變更。

## 關鍵重點
- **合成數據突破電信 AI 訓練瓶頸**：54% 的電信營運商將資料相關問題列為最大障礙，因最有價值的網路與客戶資料過於敏感而無法直接使用。軟銀（SoftBank）運用 NVIDIA NeMo Safe Synthesizer 與 NeMo Anonymizer 生成隱私保護的合成數據集，反映真實網路效能與配置的結構與分佈，用於微調其大型電信模型並建構專屬網路 Agent，在不暴露原始客戶紀錄的前提下擴大訓練資料規模。
- **安全自主 Agent 的多樣應用場景**：NemoClaw 藍圖與 OpenShell 安全執行環境提供政策型防護柵欄與沙盒存取，讓 Agent 能在嚴格 SLA、變更管理與監管約束下運作。合作案例包括：（1）AdaptKey——安全加固的長程 Agent 用於 5G 網路自癒合，檢測安全與連線問題並提交修復請求至 KeySmith 平台執行；（2）Amdocs——主動式客戶服務 Agent 監測漫遊套餐用量並執行業務政策內的行動，以及自主資料科學 Agent 分析客戶遷移資格；（3）NTT DATA——使用 Nemotron 模型建構長程異常檢測 Agent，追蹤長期效能趨勢並升級至研究 Agent 進行細粒度分析；（4）ServiceNow Project Arc——整合郵件、日誌與診斷資料的自主網路營運中心 Agent，全週期管理事件回應；（5）TCS——多保真度「AI 感應器」架構，以 Nemotron 與 NV-Tesseract 時序模型廣泛掃描問題並觸發深度診斷。
- **加速模擬打造 RAN 數位雙生**：GPU 加速模擬成為 Agent 決策支援的關鍵環節，讓 Agent 能在接近實時的虛擬環境中驗證建議再對真實網路執行操作。Forsk 在 RTX PRO 6000 Blackwell Server Edition GPU 上實現射線追蹤級無線電傳播模擬準確度，速度達 CPU 基線的 200 倍，用於 RAN 數位雙生的即時最佳化；VIAVI 將 TeraVM AI RAN 場景生成器從 CPU 遷移至 GPU，模擬吞吐量提升數量級；KDDI 與 NVIDIA、Keysight、Samsung 合作以 Aerial Omniverse 數位雙生技術，讓多個自主 Agent 安全模擬 6G 時期的 RAN「假設分析」場景。

## 結論
電信產業的自動化已不再是終點，而是自主性的起飛平台——NVIDIA 以合成數據解決訓練資料隱私困境、以 NemoClaw 與 OpenShell 提供安全 Agent 執行環境、以 GPU 加速模擬打造 RAN 數位雙生，三管齊下讓電信營運商能建構全天候、可審計、符合政策的自主網路營運體系。從軟銀的電信模型、ServiceNow 的事件回應 Agent 到 KDDI 的 6G 數位雙生，電信自主網路的藍圖已從概念走向實戰部署，為消費者和企業端帶來更豐富、更可靠的 AI 驅動服務。

---
