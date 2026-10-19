# Code, Test, and Deploy on One Machine with NVIDIA RTX Spark

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-10-16
- **原文連結**: https://developer.nvidia.com/blog/code-test-and-deploy-on-one-machine-with-nvidia-rtx-spark/

## 核心主題
NVIDIA RTX Spark 結合 GB10 系統晶片與高達 128GB 統一記憶體，讓開發者能在單一電腦上運行本地編碼代理、測試並部署 AI 應用。该平台提供比 Intel Panther Lake 12Xe 快 4.6 倍的編碼代理性能、2.7 倍的微調速度和 1.8 倍的程式碼編譯速度。

## 關鍵重點
- **單一設備完整開發工作流**：RTX Spark 筆記型電腦和小型桌面電腦讓開發者能在單一設備上完成所有開發工作，支援 Windows 和 Windows Subsystem for Linux 兩種模式，無需程式碼遷移。
- **卓越的性能表現**：相比 Intel Panther Lake 12Xe，RTX Spark 在編碼代理、模型微調和程式碼編譯方面分別提供 4.6 倍、2.7 倍和 1.8 倍的性能提升。
- **擴展的 Windows on Arm 軟體堆疊**：NVIDIA 與 Microsoft 合作推出首款 PyTorch-CUDA 版本、原生 Python 3.15、超過 2,000 個 Conda 套件，以及超過 97% 的頂級 Python 套件提供 Arm 相容版本。
- **本地編碼代理支援**：支援 GitHub Copilot、Pi、Hermes、OpenClaw 等頂級編碼代理，並推出 Nemotron 3.5 Bolt 74B-A9B 24GB 模型，可通過 llama.cpp、vLLM、Ollama、Unsloth 和 LM Studio 運行。
- **決策模型突破**：llama.cpp 和 Unsloth 現在支援決策模型，使 AI 代理的決策速度比傳統推理循環快達 200 倍。
- **媒體 AI SDK 可用**：NVIDIA AI for Media SDKs 提供影片超解析、影像生成和 TrueHDR 功能，可通過 PyPI 和 NGC 獲取。

## 結論
NVIDIA RTX Spark 重新定義了 AI 開發工作流，將原本分散在筆記型電腦、雲端 API 和雲端虛擬機的工作流整合到單一設備上。透過強大的 GPU 性能和擴展的軟體生態系統，開發者可以更高效地進行 AI 應用開發、測試和部署，同時降低雲端依賴和 Token 消耗。
---
