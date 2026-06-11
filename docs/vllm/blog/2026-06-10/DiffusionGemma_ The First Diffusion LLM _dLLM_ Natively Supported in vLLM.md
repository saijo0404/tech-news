---
# DiffusionGemma: The First Diffusion LLM (dLLM) Natively Supported in vLLM

- **來源**: vLLM Blog
- **發布日期**: 2026-06-10
- **原文連結**: https://vllm.ai/blog/2026-06-10-diffusion-gemma

## 核心主題
vLLM 宣布原生支援 Google DiffusionGemma——首款在 vLLM 中獲得完整支援的離散擴散語言模型（dLLM），透過 ModelState 抽象、自訂抽樣器與動態序列因果注意力，實現與 Hugging Face 參考實作相同的準確度與高效能批次服務。

## 關鍵重點
- **擴散式解碼架構與熵界限去噪**：DiffusionGemma 每次平行去噪 256 個 token 的畫布，以 encoder（因果注意力）和 decoder（雙向注意力）兩種模式共享同一組權重；透過熵界限（entropy-bound）規則依信心順序接受 token，搭配自條件（self-conditioning）將上一輪 softmax 分佈以閘控 MLP 形式回饋，使模型在數個去噪步驟內收斂。
- **ModelState 介面與 speculative decoding 路徑重構**：vLLM 將 DiffusionGemma 插入現有的 speculative decoding 路徑中，透過 ModelState 定義 `prepare_inputs()`、`prepare_attn()`、`custom_sampler()` 等 hook，使核心排程器與模型執行器無需修改即可支援非自回歸模型；新增的 DiffusionSampler 以單一 `@torch.compiled` 函式處理 prefill、denoise 與 commit 三種階段，並透過 `num_sampled = 0` 的標記將去噪迴圈完全封裝在 speculative decoding 帳務系統內。
- **動態序列因果注意力與量化支援**：為處理同一批次中不同階段請求的注意力模式切換（因果 vs 雙向、單向 vs 對稱滑動視窗），vLLM 實作 per-sequence 動態因果注意力，支援 Triton Attention 與 FlashAttention 4；同時透過 LLM Compressor 提供 FP8 與 NVFP4 量化檢查點，在 H200 上 FP8 模型達到 1,288 tokens/秒（約為標準自回歸基準的 6 倍）。

## 結論
這項由 Google DeepMind 與 vLLM 團隊緊密合作的成果不僅讓 DiffusionGemma 在 vLLM 中實現高效能低延遲服務，更透過 ModelState 設計為未來擴散語言模型的整合提供了可複製藍圖，同時支援量化版本以進一步降低部署成本。

---
