# DiffusionGemma：vLLM 首度原生支援的首款擴散式語言模型（dLLM）

- **來源**: vLLM Blog
- **發布日期**: 2026-06-10
- **原文連結**: https://vllm.ai/blog/2026-06-10-diffusion-gemma

## 核心主題
vLLM 宣布原生支援 Google DiffusionGemma，這是第一款在 vLLM 中實現的離散擴散語言模型（dLLM），透過改寫編碼方式在單張 H100/H200 上達到超越傳統自回歸模型數倍的生成速度。

## 關鍵重點
- **擴散式生成架構**：DiffusionGemma 使用 26B 参数的 MoE 模型（每次推理僅激活 3.8B），以「固定畫布（256 tokens）平行去噪」取代逐 token 生成的自回歸模式，將解碼瓶頸從記憶體頻寬轉移至運算，在低批次大小下可達 1,000–1,288 tokens/秒（H100/H200），約為自回歸基準的 5–6 倍。
- **vLLM 整合設計**：透過 model runner v2 的 ModelState 抽象層，vLLM 以極小改動（仅需 ModelState 與 DiffusionSampler）即可支援擴散模型。開發者加入新 dLLM 時，只需實作 ModelState 並註冊，不需更動調度器或共享基礎設施，為未來擴散語言模型的整合立下藍圖。
- **關鍵技術創新**：（1）熵閾值去噪——以位置預測的熵值決定保留哪些 token，逐步收斂整塊內容；（2）自我條件化（self-conditioning）——將上一步的軟機率分布回饋給模型，加速收斂；（3）動態每序列因果注意力——同一批次內混合因果與雙向注意力，並支援 FlashAttention 4 與 Triton 後端及滑動窗口注意力；（4）提供 FP8 與 NVFP4 量化檢查點，在 Hugging Face RedHatAI 倉庫提供下載。

## 結論
vLLM 對 DiffusionGemma 的原生支援，不僅讓開發者能以最少的設定部署這款創新型語言模型，也展示了擴散式生成在低延遲互動應用中的巨大潛力。配合量化檢查點與完善的注意力後端，這為下一代高效能語言模型推理打開了新的可能性。
