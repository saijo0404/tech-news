# DiffusionGemma: 4x faster text generation

- **來源**: DeepMind Blog
- **發布日期**: 2026-06-10
- **原文連結**: https://deepmind.google/blog/diffusiongemma-4x-faster-text-generation/

## 核心主題
Google DeepMind 發布 DiffusionGemma——一款以 Apache 2.0 授權開放的實驗性 26B MoE 文字擴散語言模型，透過平行生成 256 個 token 的區塊而非逐字序列生成，在專用 GPU 上實現最高 4 倍的推論加速，專為速度敏感型互動式本地工作流程設計。

## 關鍵重點
- **平行生成突破記憶體頻寬瓶頸**：DiffusionGemma 將解碼瓶頸從記憶體頻寬轉向計算能力，在單張 NVIDIA H100 上達 1,000+ tokens/秒、GeForce RTX 5090 上達 700+ tokens/秒；作為 26B 總參數的 MoE 模型，推論時僅激活 3.8B 參數，量化後可裝入消費級 GPU 的 18GB VRAM；雙向注意力機制使每個 token 可關注所有其他 token，對行內編輯、程式碼填充、胺基酸序列等非線性領域具有顯著優勢。
- **文字擴散的工作原理**：類似影像生成的擴散過程，模型從隨機佔位符 token 畫布開始，經過多次迭代逐步鎖定正確的 token 並利用已鎖定的 token 作為上下文線索來精修其餘部分，最終使文本收斂為高品質輸出；模型可反覆自我修正，一次性評估整個文本區塊來即時修復錯誤（如完美關閉複雜 markdown 格式）。
- **實驗性質與生態系支援**：因優先考慮速度與平行生成，整體輸出品質低於標準 Gemma 4，建議高品質應用仍使用 Gemma 4；此加速優勢在低到中批量大小、單加速器的本地推論場景中最顯著，高 QPS 雲端服務中自回歸模型仍具成本優勢；已獲 MLX、vLLM、Hugging Face Transformers 等工具支援，並與 NVIDIA 合作針對消費級與企業級硬體最佳化，包括 NVFP4 4 位元浮點加速。

## 結論
DiffusionGemma 開啟了文字生成從逐字打字機轉向同時印表機的新範式，特別適合行內編輯、快速迭代與生成非線性文本結構等互動式本地工作流程；模型權重已於 Hugging Face 開放，並提供 Unsloth、Hackable Diffusion、NVIDIA NeMo 等多種微調途徑供研究與開發者探索。

---
