# Announcing Day 0 Support for NVIDIA Nemotron 3.5 Super VL on vLLM

- **來源**: vLLM Blog
- **發布日期**: 2026-10-15
- **原文連結**: https://vllm.ai/blog/2026-10-15-nemotron-3-5-super-vl-vllm

## 核心主題
vLLM 正式支援 NVIDIA Nemotron 3.5 Super VL 模型，這是一個結合多模態理解與高準確度執行的開源模型，可提升長期代理任務的效率與準確性。

## 關鍵重點
- **模型架構**：120B 參數混合專家架構，120B 總參數中 120B 為活躍參數，支援文本、圖像、文檔和視頻理解
- **部署優化**：支援多令牌預測 (MTP) 和 NVFP4 量化，可提升推理效率
- **應用場景**：適用於客戶服務、文檔智能、企業生產力、視頻理解和網頁研究等多種代理任務
- **性能優勢**：相比同級開源模型，單 GPU 推理速度快 5 倍，任務完成速度快 4 倍
- **部署方式**：可通過 vLLM 服務，支援 OpenAI 相容 API，可在多種 NVIDIA 硬體上運行

## 結論
vLLM 為 NVIDIA Nemotron 3.5 Super VL 提供了 Day 0 支援，使開發者能夠快速部署和優化多模態代理工作流。
---