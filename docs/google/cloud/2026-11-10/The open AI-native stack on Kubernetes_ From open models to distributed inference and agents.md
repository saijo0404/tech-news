# The open AI-native stack on Kubernetes: From open models to distributed inference and agents

- **來源**: Google Cloud Blog Developers & Practitioners
- **發布日期**: 2026-11-10
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/the-open-ai-native-stack-on-kubernetes-from-open-models-to-distributed-inference-and-agents/

## 核心主題
這篇文章介紹了 Google Cloud 推出的一套開源 AI 原生堆疊，旨在將 AI 工作負載從研究原型擴展到大型多租戶生產環境，並提供可嘗試的樣本 manifest。

## 關鍵重點
- **OpenRL**: Kubernetes 原生的後訓練服務，簡化 RL 後訓練並最大化加速器利用率，透過 cooperative accelerator time-slicing 避免硬體閒置。
- **llm-d 1.0**: 開源分佈式推理控制平面，提供前綴緩存感知路由、分散式服務和多級 KV 緩存管理，將 KV cache hit rates 從 35% 提升至 70%。
- **KubeRay**: Kubernetes 原生的 Ray 集群管理工具，提供彈性自動擴展和 Kueue 驅動的排程，整合多租戶公平共享與優先預empt。
- **Agent Substrate & gVisor**: 提供多轉 AI 工作流的生命週期管理和執行目標，以及基於用戶空間的緩存隔離，確保未信任代碼的安全執行。
- **TorchTPU**: 提供原生 PyTorch 支援，可在 Cloud TPU 和 GPU 上運行，實現 TPU 與 NVIDIA GPU 的零日對等性。

## 結論
這套開源堆疊成功解決了傳統容器基礎設施在擴展 RL 後訓練、分佈式推理和自主代理執行時面臨的挑戰，並已在 KubeCon + CloudNativeCon North America 2026 上展示。測試顯示，使用 OpenRL 將模型準確率從 50% 提升至 70%，同時實現動態資源共享與多租戶管理。

---

檔案已成功儲存至指定路徑。