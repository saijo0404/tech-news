# ModelExpress: Distributing Model Artifacts at the Speed of Light

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-07-24
- **原文連結**: https://developer.nvidia.com/blog/modelexpress-distributing-model-artifacts-at-the-speed-of-light/

## 核心主題
NVIDIA ModelExpress (MX) 透過自動選擇最快權重載入路徑（優先使用 GPU 間 P2P RDMA 傳輸），大幅加速模型權重與核心函數快取分佈，顯著降低冷啟動時間。

## 關鍵重點
- 優先使用 NIXL 進行 GPU 到 GPU 的直接 P2P RDMA 傳輸，避免不必要的物存儲和主機記憶體存取
- 支援多線程串流、原子分佈式快取、GPUDirect 儲存等先進策略，自動優化冷啟動和權重移動
- 整合 vLLM、SGLang、Dynamo 等框架，並透過 VMM 快域註冊優化記憶體註冊開銷

## 結論
ModelExpress 透過智能路徑選擇和高效傳輸機制，將 DeepSeek-V4 Pro 模型的冷啟動時間從 8 分鐘大幅縮短至 1 分 44 秒，為大規模 LLM 部署帶來顯著性能提升。
---