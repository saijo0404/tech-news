# TorchTPU is now open source: Run native PyTorch on TPUs

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-21
- **原文連結**: https://cloud.google.com/blog/topics/ai-infrastructure/torchtpu-is-now-open-source-run-native-pytorch-on-tpus/

## 核心主題
Google 正式開放 TorchTPU 源碼，讓 TPUs 成為 PyTorch 的原生執行選項，並與 PyTorch 生態系多項開源專案深度整合，提供從訓練到推理的全流程優化。

## 關鍵重點
- **原生 PyTorch 支援**：TorchTPU 與 PyTorch 團隊合作開發，讓現有 PyTorch 工作流可無縫運行於 TPUs，支援 eager mode 調試與 torch.compile 生產級優化。
- **開源生態整合**：與 Hugging Face、vLLM、SGLang、llm-d、TorchTitan、VeRL、Ray 等開源專案合作，提供從模型訓練到推理服務的全套工具。
- **推理優化**：透過 vLLM、SGLang 等服務引擎與 Kubernetes 原生fleet路由，優化推理成本與延遲，支援高吞吐量與低延遲需求。
- **大規模訓練**：TorchTitan 支援在最多 8,192 台 Ironwood TPUs 上進行大模型訓練，MFU 達 52%，支援 Llama 3、Qwen 3 等大模型預訓練。
- **部署靈活性**：LiteRT 加入 PyTorch 生態系，支援邊緣設備部署；TPU agent suite 提供自動化調試與性能優化工具。

## 結論
TorchTPU 的開放源碼化與生態系整合，大幅降低 TPUs 的使用門檻，讓開發者能更靈活地選擇硬體架構，加速 AI 模型開發與部署。

---

檔案已成功儲存至指定路徑。