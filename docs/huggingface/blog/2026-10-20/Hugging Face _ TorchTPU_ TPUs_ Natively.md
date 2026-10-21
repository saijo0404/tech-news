# Hugging Face ❤️ TorchTPU: TPUs, Natively

- **來源**: Hugging Face Blog
- **發布日期**: 2026-10-20
- **原文連結**: https://huggingface.co/blog/hf-torchtpu

## 核心主題
Hugging Face 推出 TorchTPU，讓 PyTorch 原生支援 Google TPU 硬體，使 Transformers、Diffusers 等主流庫能直接在 TPU 上運行，無需額外移植或學習 JAX。

## 關鍵重點
- **極簡使用方式**：只需將模型傳送至 `device_map="tpu"`，即可在 TPU 上運行 PyTorch 代碼，無需改寫邏輯。
- **原生生態整合**：Transformers、Diffusers 和 Kernels 庫已原生支援 TPU，取代了過往需要 torch_xla 或 Optimum TPU 的複雜流程。
- **性能優化**：提供 Pallas 優化核函式與 torch.compile 整合，在批量推理時可達 21.5 倍速度提升（如 Qwen3-30B 模型）。
- **測試品質**：Transformers 測試套件在 TPU 上通過率達 96.5%，持續回饋錯誤以改善模型與庫的相容性。

## 結論
TPU 不再是 PyTorch 用戶的邊緣選項，而是原生支援的一等公民設備。透過 TorchTPU，開發者可以像使用 GPU 一樣直接使用 TPU，大幅降低 AI 加速器的使用門檻。

---