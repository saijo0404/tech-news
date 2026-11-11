# Agent Substrate: Advancing Kubernetes for Agents at Scale

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-11-10
- **原文連結**: https://developer.nvidia.com/blog/agent-substrate-advancing-kubernetes-for-agents-at-scale/

## 核心主題
Agent Substrate 是一個開源代理基礎設施解決方案，透過 Kubernetes 實現高密度代理執行，支援編程助手、強化學習和 GPU 沙盒等三種主要工作負載。

## 關鍵重點
- **代理多路複用技術**：透過檢查點（checkpoint）技術將多個代理会话 multiplex 到少量 Kubernetes worker Pods 上，閒置時保存完整記憶體和檔案系統狀態，恢復時無需重新啟動
- **三種主要工作負載**：
  1. 編程助手：交替執行 LLM 調用與檔案操作（複製倉庫、編輯檔案、執行測試）
  2. 強化學習後訓練：突發式 CPU 密集型環境（編譯器、瀏覽器、模擬器）
  3. 研究用 GPU 沙盒：編譯 CUDA 代碼、性能測試和數值計算
- **上游貢獻**：
  - 請求停車機制：當所有 worker 繁忙時排隊等待而非立即失敗
  - 容器資源限制：防止單個容器佔滿記憶體並影響鄰居容器
  - GPU 狀態暫停/恢復設計：基於 Kubernetes Dynamic Resource Allocation (DRA)，支援 NVIDIA GPU 並可擴展到其他硬體
- **與 NVIDIA Dynamo 整合**：Dynamo 負責推理調度，Agent Substrate 管理代理環境，兩者透過推理信號（如預估首次 token 時間、GPU 池飽和度）交換資訊以優化資源利用
- **平台整合**：運行於 NVIDIA DSX AI Factory Platform，Substrate 作為獨立 CNCF Sandbox 項目與 DSX OS 組件整合

## 結論
Agent Substrate 已捐贈給 Cloud Native Computing Foundation (CNCF)，是安全強化、零信任運行的代理沙盒解決方案，可安全運行百萬級代理與工具，密度比標準容器高 10 倍。隨著 NVIDIA Dynamo 和 KAI Scheduler 的整合，正在構建完整的 AI 代理平台生態系統。

---