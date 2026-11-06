# Powering open infrastructure for autonomous agents

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-06
- **原文連結**: https://cloud.google.com/blog/products/containers-kubernetes/open-infrastructure-for-autonomous-agents-comes-to-cncf/

## 核心主題
Google 將三個開源專案（Agent Substrate、gVisor、OpenRL）捐贈給 CNCF，以支援自主代理的開源基礎設施架構。

## 關鍵重點
- **Agent Substrate 1.0 已推出**：支援百萬級沙盒，密度提升10倍，閒置代理可在500毫秒內存儲/恢復，解決代理等待模型推理或外部API時的資源浪費問題。
- **gVisor 提供輕量級用戶空間隔離**：隔離未審查的程式碼，支援GPU/TPU，不依賴巢狀虛擬化，可部署在任何Linux節點上。捐贈給CNCF後，更多貢獻者（如Ant Group、Modal、OpenAI）加入維護。
- **OpenRL 提供 Kubernetes 上的純 Python RL 訓練迴路**：支援簡單 Python 原語、可插拔引擎和 Kubernetes 排程，與 llm-d 搭配實現 GPU 時間切片，優化 RL 後訓練效率。

## 結論
透過將這些專案捐贈給 CNCF，Google 確認了對開放協作和共同投資的承諾，並為雲端供應商、硬體供應商和獨立軟體公司創造了平等參與自主工作負載未來成長的機會。這套開源堆疊將加速自主工作負載的發展和採用，類似於 Kubernetes 在2010年代帶來的影響。

---