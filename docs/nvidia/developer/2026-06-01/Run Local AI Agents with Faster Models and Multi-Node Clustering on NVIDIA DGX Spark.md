# 在 NVIDIA DGX Spark 上使用更快模型與多節點叢集運行本地 AI 代理

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-05-31
- **原文連結**: https://developer.nvidia.com/blog/run-local-ai-agents-with-faster-models-and-multi-node-clustering-on-nvidia-dgx-spark/

## 核心主題
NVIDIA 在 Computex 2026 宣布 DGX Spark 的多項更新，包括簡化的 NemoClaw 安裝流程、Qwen3.6-35B 模型效能提升與 NVIDIA Sync 叢集助理，讓開發者能從開箱到運行本地 AI 代理，大幅縮短設置時間並擴展計算規模。

## 關鍵重點
- **從開箱到運行 AI 代理的簡化流程**：透過單一 `curl` 指令安裝 NemoClaw，自動設定 Ollama、Qwen3.6-35B 模型與 OpenShell 安全沙盒環境，並提供四種即用的預設代理（每日新聞摘要、軟體開發代理、文件審查代理、行事曆協商代理），搭配系統提示詞編輯與工具權限調整，讓開發者快速客製化。
- **Qwen3.6-35B 模型效能提升 2.6 倍**：透過 NVIDIA NVFP4 量化權重、MTP 最佳化、vLLM CUDA Graph 支援 FlashInfer、BF16 autotuning 等多項技術優化，在 DGX Spark 上實現整體吞吐效能提升 2.6 倍。
- **NVIDIA Sync 叢集助理簡化多節點擴展**：針對單一裝置算力不足的需求，Sync 叢集助理自動化將 2 至 4 台 DGX Spark 連接為高頻寬叢集（2 節點提供 256 GB 統一記憶體可運行約 400B 參數模型，4 節點提供 512 GB），透過引導式工作流處理 ConnectX-7 網路設定、拓撲偵測、頻寬驗證與 SSH 信任建立，支援 2 節點直連、3 節點環狀與 2-4 節點交換器連接等拓撲。

## 結論
DGX Spark 的這些更新消除了生產級本地 AI 代理的兩大痛點——首個代理的上手時間與大模型的運算需求，讓開發者能在安全的本機環境中快速部署、微調與擴展 AI 代理，為企業級自主代理工作負載提供從單機到多節點的完整解決方案。
