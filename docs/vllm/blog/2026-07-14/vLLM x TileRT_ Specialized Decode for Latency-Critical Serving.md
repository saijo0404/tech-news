# vLLM x TileRT: Specialized Decode for Latency-Critical Serving

- **來源**: vLLM Blog
- **發布日期**: 2026-07-14
- **原文連結**: https://vllm.ai/blog/2026-07-14-vllm-tilert-pd

## 核心主題
vLLM 與 TileRT 整合，提供專用的解碼引擎以優化延遲敏感型工作負載，透過解耦架構實現零修改部署。

## 關鍵重點
- 採用解耦架構，prefill 使用 vLLM，decode 使用 TileRT，讓延遲敏感型工作負載（如互動式代理、實時語音）能獲得最佳性能
- TileRT 專注於提升單一使用者的解碼速度，與 vLLM 原生解碼引擎各有專長，可根據工作負載需求選擇
- 透過 vLLM V1 的公開連接介面實現零修改整合，無需分叉或修改現有部署，僅透過路由將特定流量導向 TileRT 解碼池
- 支援 GLM-5/5.1 和 DeepSeek-V3.2 等模型，使用 RDMA 一側寫入實現高效資料傳輸，解碼速度在 8× NVIDIA B200 上可達峰值

## 結論
此整合展示了現代推理堆疊的趨勢：從單一引擎轉向由多個專用引擎組成的可擴展架構，vLLM 的連接介面使這種組態成為可能，為延遲敏感型工作負載提供了更靈活的解決方案。

---