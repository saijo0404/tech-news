# NVIDIA Vera Rubin NVL72 Leads Agentic Inference Performance on MLPerf Endpoints v1.0

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-11-16
- **原文連結**: https://developer.nvidia.com/blog/nvidia-vera-rubin-nvl72-leads-agentic-inference-performance-on-mlperf-endpoints-v1-0/

## 核心主題
NVIDIA Vera Rubin NVL72 在 MLPerf Endpoints v1.0 測試中，以超過 10 倍的每千瓦吞吐量領先 NVIDIA GB300 NVL72，展現了針對代理推理優化的硬體與軟體優化。

## 關鍵重點
- Vera Rubin NVL72 在 Kimi K3、DeepSeek-V4.1-Flash 和 Qwen3.6-35B-A3B 模型上，分別實現 10 倍、9 倍和 5 倍的每千瓦吞吐量提升，同時保持 50 tokens/秒/使用者的最低終端至終端互動性。
- NVIDIA Rubin GPU 結合 HBM4 記憶體、Tensor Cores 和第六代 NVLink，支援代理推理需求，並透過上下文感知的服務技術（如前綴快取、狀態重用和 NVIDIA Dynamo 路由）減少冗餘計算。
- 模型特定的 GPU 執行優化（如 DeepSeek 的 MegaMoE 核和 Qwen 的多 token 預測）減少資料移動和序列解碼步驟，提升推理效能。

## 結論
Vera Rubin 平台透過硬體與軟體的協同優化，為代理 AI 工作負載提供更高效能的推理基礎設施，使組織能在相同電力預算內運行更多代理，同時滿足響應性要求。
---