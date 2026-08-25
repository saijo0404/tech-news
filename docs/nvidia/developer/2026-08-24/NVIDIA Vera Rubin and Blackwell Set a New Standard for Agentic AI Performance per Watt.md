# NVIDIA Vera Rubin and Blackwell Set a New Standard for Agentic AI Performance per Watt

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-08-24
- **原文連結**: https://developer.nvidia.com/blog/nvidia-vera-rubin-and-blackwell-set-a-new-standard-for-agentic-ai-performance-per-watt/

## 核心主題
NVIDIA Vera Rubin 和 Blackwell 系列在代理 AI 推理性能每瓦特方面設立了新標準，Vera Rubin NVL72 比 GB300 NVL72 高出 30 倍，而 GB300 NVL72 對大型 MoE 模型則高出 80 倍。

## 關鍵重點
- **代理 AI 工作負載特性**：代理 AI 從單次互動擴展為多步驟工作流，需要處理長上下文、KV 快取重疊、工具調用間隙和動態並行，傳統固定序列長度基準已不再適用。
- **AgentX 基準測試**：SemiAnalysis 開發的 AgentX 基準使用重播的生產環境程式碼代理會話，準確評估加速器服務代理推理的效率，測量每兆瓦的 token 產出量。
- **Vera Rubin NVL72 突破**：在 AgentX DeepSeek V4-Pro 工作負載下，Vera Rubin NVL72 在 160 tokens/秒/用戶的互動水平下，比 GB300 NVL72 高出 30 倍的 AI 工廠吞吐量每兆瓦。
- **GB300 NVL72 優勢**：對 DeepSeek V4 Pro 1.6T 模型高出 H200 NVL8 15 倍，對 Kimi K3 2.8T 大型 MoE 模型則高出 80 倍，單位成本降低 10 倍。
- **系統級優化技術**：效率提升來自 MoE 服務運行時（SGLang、TensorRT-LLM、vLLM）、DeepGEMM 核、混合精度格式（MXFP4、MXFP8）、NVIDIA Dynamo 會話感知服務堆疊和 NVLink 擴展互連。

## 結論
NVIDIA 透過 Vera Rubin 和 Blackwell 平台的系統級優化，成功將固定電力預算轉換為更有用的代理輸出，為 AI 工廠帶來顯著的性能和成本優勢，同時維持可接受的用戶體驗。

---