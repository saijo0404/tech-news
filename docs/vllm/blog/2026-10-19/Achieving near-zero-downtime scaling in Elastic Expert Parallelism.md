# Achieving near-zero-downtime scaling in Elastic Expert Parallelism

- **來源**: vLLM Blog
- **發布日期**: 2026-10-19
- **原文連結**: https://vllm.ai/blog/2026-10-19-elastic-ep-near-zero-downtime

## 核心主題
vLLM 透過引入 NIXL EP 和異步準備機制，實現了彈性專家並行（Elastic EP）架構下的近乎零停機擴展能力，大幅減少擴展 GPU 時的服務中斷時間。

## 關鍵重點
- 傳統擴展方式需要重新啟動服務，停機時間長達 197 秒；使用 NIXL EP 後停機時間降至 0.82 秒（16→20 GPU）和 1.96 秒（20→16 GPU）
- 採用異步準備與準備/提交優化，在背景準備新 worker 的同時繼續服務請求
- NIXL EP 允許在位擴展專家並行通信，重using 相同的通信緩衝區和連接，避免無效化已捕捉的 CUDA 圖
- 加入的 worker 可以獨立準備 CUDA 圖，不需要現有 worker 參與
- 在 DeepSeek V4 Pro 測試中，服務級別目標（SLO）全程符合要求，p95 首 token 時間低於 5 秒

## 結論
這項技術使大規模 LLM 服務能夠在擴展 GPU 資源時幾乎不影響服務性能，為彈性雲基礎設施提供了重要突破。
---
