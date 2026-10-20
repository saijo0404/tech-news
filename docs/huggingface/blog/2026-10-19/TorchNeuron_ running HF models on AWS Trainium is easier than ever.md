# TorchNeuron: running HF models on AWS Trainium is easier than ever

- **來源**: Hugging Face
- **發布日期**: 2026-10-19
- **原文連結**: https://huggingface.co/blog/hf-torchneuron

## 核心主題
Hugging Face 推出 TorchNeuron，讓在 AWS Trainium 上運行 Hugging Face 模型變得比以往更容易，提供原生 PyTorch 支援。

## 關鍵重點
- TorchNeuron 是 PyTorch 插件，提供 Trainium 的新原生後端，支援 eager mode、torch.compile 和原生分佈 API（如 FSDP 和 TP）
- Hugging Face 庫（Transformers、Diffusers、Accelerate、PEFT、TRL）現在可直接在 Trainium 上運行，無需通過 Optimum Neuron
- 支援範圍擴大：Transformers 推理支援 89% 的頂部 100 個文字生成模型架構（Optimum Neuron 僅支援 46%）
- 訓練和推理都更簡單：使用相同的 Hugging Face 庫，只需少量 Neuron 特定設定
- 模型可移植性：訓練好的模型可推送到 Hugging Face Hub，可在任何硬體上運行
- 支援更多模型：Diffusers 中的許多管道（如 FLUX.1-dev、Qwen-Image 系列）支援 Tensor Parallelism
- 自定義核函數：用戶可使用 Neuron 核函數介面（NKI）創建自定義操作

## 結論
TorchNeuron 通過原生集成和更簡單的 API，大幅降低了在 AWS Trainium 上運行 Hugging Face 模型的門檻，使開發者可以更輕鬆地部署和分享模型。
---
