---
# DiffusionGemma: 4x faster text generation

- **來源**: Google Blog
- **發布日期**: 2026-06-10
- **原文連結**: https://blog.google/innovation-and-ai/technology/developers-tools/diffusion-gemma-faster-text-generation/

## 核心主題
Google 推出實驗性語言模型 DiffusionGemma，採用文字擴散（text diffusion）技術，突破傳統逐字生成的限制，在專用 GPU 上實現高達 4 倍的生成速度。

## 關鍵重點
- **平行生成取代順序預測**：DiffusionGemma 不再像傳統 LLM 那樣一個接一個地生成 token，而是每次前向傳播同時生成 256 個 token，將解碼瓶頸從記憶體頻寬轉移到運算能力，在單一 NVIDIA H100 上可達 1000+ tokens/秒，RTX 5090 上達 700+ tokens/秒。
- **雙向注意力與自我修正**：每個 token 都能注意到其他所有 token，對於非線性任務（如程式碼補全、Markdown 格式化、數值圖譜）有顯著優勢；模型也能整段評估並反覆修正自身輸出。
- **輕量級 MoE 架構與硬件優化**：總參數 26B、推理時僅激活 3.8B，量化後可在 18GB VRAM 的消费級 GPU 上運行；與 NVIDIA 合作針對 Hopper/Blackwell 架構進行 NVFP4 4-bit 加速優化。

## 結論
DiffusionGemma 以 Apache 2.0 授權開源，專為需要極低延遲的本地互動式工作流設計（如行內編輯、快速迭代），但由於優先追求速度，其整體生成品質仍低於標準 Gemma 4 模型；適合需要即時互動的場景，高品質產出則建議使用傳統自回歸模型。

---
