# Enabling Private High-Performance Production AI Inference with NVIDIA Confidential Computing

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-09-22
- **原文連結**: https://developer.nvidia.com/blog/enabling-private-high-performance-production-ai-inference-with-nvidia-confidential-computing/

## 核心主題
這篇文章探討如何在 NVIDIA Confidential Computing (CC) 環境下實現高性能 AI 推理，並介紹 TensorRT LLM 的 CC-aware 優化策略。

## 關鍵重點
- 使用 confidential virtual machines (CVMs)、confidential GPUs 和 encrypted NVLink 來保護敏感數據，使 AI 推理能在可信環境中運行
- 在 CC 環境下，TensorRT LLM 針對數據移動、核內自調優和多 GPU 通信進行了 CC-aware 優化，以減少性能損失
- 測試顯示 CC 開啟後保留了 96.1-98.2% 的吞吐量，TPOT 延遲增加僅 1.2-4.3%，證明 CC 對性能影響可控
- 建議將安全配置和推理優化視為完整的工程努力，需針對特定工作負載進行 CC-on 與 CC-off 的對比測試

## 結論
NVIDIA Confidential Computing 可安全地運行 AI 推理，但需要框架和環境的協同優化來保持高性能。對於 AI 平台工程師，應將安全配置與推理優化視為完整的部署問題，並使用 NVIDIA Trusted Computing 文檔進行規劃。

---