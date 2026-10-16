# Scale Agentic Coding Workflows with Meta's Muse Spark Open on NVIDIA GB300 NVL72

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-10-15
- **原文連結**: https://developer.nvidia.com/blog/scale-agentic-coding-workflows-with-metas-muse-spark-open-on-nvidia-gb300-nvl72/

## 核心主題
Meta 推出 Muse Spark Open 編碼優化模型，專為代理編碼工作流設計，運行於 NVIDIA GB300 NVL72 平台上。

## 關鍵重點
- Muse Spark Open 是 816B 混合專家(MoE)模型，每 token 激活 42B 參數，具有 1M token 上下文窗口
- 支持多模態理解（音頻、視頻、圖像、文檔），原生處理交叉模態
- 在 NVIDIA GB300 NVL72 上運行，每 GPU 每秒可達 50K token，每用戶每秒 600 token
- 使用 NVFP4 檢查點優化，利用 NVIDIA Blackwell Ultra 的 FP4 Tensor Core 加速
- 支持代理工作流：規劃、執行、觀察、自我修正，可跨整個專案進行多步驟任務

## 結論
Muse Spark Open 是專為代理編碼工作流設計的開源模型，結合了 Meta 的編碼優化與 NVIDIA 的 Blackwell 硬體加速，為開發者提供高吞吐量、低延遲的生產級 AI 編碼解決方案。
---
