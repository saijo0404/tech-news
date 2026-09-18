# Scaling Multi-GPU Video Captioning with PyNvVideoCodec and vLLM

- **來源**: vLLM Blog
- **發布日期**: 2026-09-18
- **原文連結**: https://vllm.ai/blog/2026-09-18-pynvvideocodec

## 核心主題
vLLM 現在支援 NVIDIA GPU 硬體視頻解碼，可將視頻標題生成任務的視頻解碼工作從 CPU 移至 GPU，大幅提升多 GPU 節點上的吞吐量。

## 關鍵重點
- 使用 PyNvVideoCodec 將視頻解碼工作從 CPU 移至 NVIDIA GPU 硬體解碼器（NVDEC），消除 CPU 瓶頸
- 支援最多 8 個 GPU 的擴展，在 8xH100 配置下，GPU 基於視頻解碼的吞吐量比 CPU 基於的視頻解碼器高出兩倍以上
- 安裝時需確保包含 PyNvVideoCodec==2.0.4 依賴，並啟動 CUDA MPS Daemon 以獲得最佳性能

## 結論
此功能已包含在標準 CUDA vLLM 發行版中，可顯著提升視頻標題生成任務的吞吐量，特別適合需要處理大量視頻數據的場景，如自動駕駛訓練系統。