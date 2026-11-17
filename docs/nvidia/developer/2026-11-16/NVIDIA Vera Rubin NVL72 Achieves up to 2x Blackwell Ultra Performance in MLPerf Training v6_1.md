# NVIDIA Vera Rubin NVL72 Achieves up to 2x Blackwell Ultra Performance in MLPerf Training v6.1

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-11-16
- **原文連結**: https://developer.nvidia.com/blog/nvidia-vera-rubin-nvl72-achieves-up-to-2x-blackwell-ultra-performance-in-mlperf-training-v6-1/

## 核心主題
NVIDIA Vera Rubin NVL72 平台在 MLPerf Training v6.1 中首次亮相，在六個七個基準測試中達成最快訓練時間，展現比優化後 GB300 NVL72 快達 2 倍的每 GPU 效能。

## 關鍵重點
- **DeepSeek-V3 671B 基準測試**: Vera Rubin NVL72 使用 1,024 GPU 僅用 4.14 分鐘完成訓練，比 GB300 NVL72 的 8.03 分鐘快 2 倍，展現最大效能提升。
- **強化學習基準測試**: 在 Qwen 3.5 397B GRPO 基準測試中，Vera Rubin NVL72 以 10.44 分鐘領先，並同時支援 TensorRT-LLM 與 vLLM 兩種推理後端，展現軟體成熟度。
- **擴展效率與架構**: 在從 256 到 1,024 GPU 擴展時維持 97% 以上效率，透過銅製 NVLink 6 背脊（每 GPU 3.6 TB/s）與 ConnectX-9 SuperNIC 實現高效能擴展。
- **軟體持續優化**: 使用更新軟體堆疊後，Llama 3.1 8B、gpt-oss 20B 與 DLRMv4 的訓練時間進一步縮短，證明硬體出貨後軟體持續優化可帶來額外效能。
- **平台普及度**: 80% 的閉門測試提交來自 20 家合作組織的 NVIDIA 平台，Vera Rubin NVL72 系統已透過雲端基礎設施合作伙伴在全球提供。

## 結論
NVIDIA Vera Rubin NVL72 的首次亮相即展現卓越訓練效能與軟體成熟度，不僅在單項基準測試中領先，更在整個 AI 訓練管道（從大規模預訓練到強化學習後訓練）提供全面支援，為開發者帶來可預測的效能提升。

---