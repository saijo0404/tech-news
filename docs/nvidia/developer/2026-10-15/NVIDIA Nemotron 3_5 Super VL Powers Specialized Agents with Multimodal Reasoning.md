# NVIDIA Nemotron 3.5 Super VL Powers Specialized Agents with Multimodal Reasoning

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-10-15
- **原文連結**: https://developer.nvidia.com/blog/nvidia-nemotron-3-5-super-vl-powers-specialized-agents-with-multimodal-reasoning/

## 核心主題
NVIDIA Nemotron 3.5 Super VL 是一款開源多模態模型，結合了推理、工具使用和視覺理解能力，可為專業化代理任務提供高效能支援。

## 關鍵重點
- 採用 120B 參數混合專家架構，每 token 激活 12B 參數，在單一 GPU 上比同級開源模型快 5 倍
- 整合推理、指令遵循、工具使用以及文字、圖像、文檔和視頻理解能力，無需部署獨立視覺語言模型
- Scale AI、Ramp 和 AI21 等組織已完成後訓練，實現推理成本降低 40 倍、延遲降低 10 倍、準確性提高 40%
- 支援 LiLiCorr 猜測解碼、NVFP4 量化、多 token 預測和上下文重用以優化推理效率
- 可透過 NVIDIA NeMo 進行監督微調、低秩適應和強化學習，針對特定領域數據進行客製化

## 結論
NVIDIA Nemotron 3.5 Super VL 為專業化代理任務提供了強大的多模態推理能力，並透過後訓練和優化技術實現了更高的準確性和效率，特別適合需要同時處理文字與視覺資訊的企業應用場景。
---