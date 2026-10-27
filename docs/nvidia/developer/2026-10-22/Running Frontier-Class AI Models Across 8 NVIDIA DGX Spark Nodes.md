# Running Frontier-Class AI Models Across 8 NVIDIA DGX Spark Nodes

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-10-22
- **原文連結**: https://developer.nvidia.com/blog/running-frontier-class-ai-models-across-8-nvidia-dgx-spark-nodes/

## 核心主題
NVIDIA DGX Spark 現在支援八節節點集群，可本地運行 frontier-class 大型語言模型，並透過優化通信後端大幅提升推理效率。

## 關鍵重點
- **記憶體容量突破**：八節節點集群提供 1TB 統一記憶體，可本地運行如 GLM 5.3 (753B) 等 frontier-class 模型，實現互動式開發。
- **優化通信後端**：Spark 優化後端 RoCEnante 在八節節點上提供 4.43 倍解碼速度提升，相比傳統後端效率提升 45%。
- **推理吞吐量提升**：解碼吞吐量從單節點約 12 tokens/秒提升至八節節點約 52 tokens/秒，支援 Qwen3.8-27B 等模型。
- **多模型路由**：NVIDIA NeMo Switchyard 可將簡單請求路由到小型模型（如 MiniCPM5 2B），整體吞吐量可提升 3 倍。
- **訓練效率**：八節節點訓練 nanochat 模型實現 7.79 倍加速，效率達 97.4%，展現接近線性擴展特性。

## 結論
NVIDIA DGX Spark 八節節點集群為本地部署大型 AI 模型提供了強大的記憶體和計算能力，透過優化通信、多模型路由和訓練效率，使 frontier-class 模型變得更加實用和可擴展。

---

## 下一步行動
- 連結多台 DGX Spark 機器建立分佈式工作負載
- 使用 vLLM 在 DGX Spark 上提供分佈式推理
- 檢視模型相容性指南和 Switchyard 編排資源
