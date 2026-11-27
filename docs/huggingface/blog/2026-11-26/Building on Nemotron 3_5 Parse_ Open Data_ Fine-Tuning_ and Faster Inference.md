# Building on Nemotron 3.5 Parse: Open Data, Fine-Tuning, and Faster Inference

- **來源**: Hugging Face Blog
- **發布日期**: 2026-11-26
- **原文連結**: https://huggingface.co/blog/nvidia/building-on-nemotron-35-parse-open-data-fine-tunin

## 核心主題
NVIDIA 基於 Nemotron 3.5 Parse 模型，分享合成訓練數據集、微調食譜和 DFlash2 預測器，以加快推理速度。

## 關鍵重點
- 開放三個訓練數據集：Synthetic Charts V1（9.98M 範例）、Synthetic Tables V1（1M 範例）、OCR Synthetic Multilingual v2（7.9M 範例），用於訓練文檔理解模型
- 採用兩階段訓練方法：SFT（監督微調）建立基本能力，RLVR（可驗證獎勵強化學習）提升準確性和一致性，使首試成功率從 0% 提升至 96.58%
- DFlash2 預測器在 H200 單通道上提升吞吐量 7.62 倍，512 並行時提升 1.52 倍，Parse 3.5 在 512 並行時從 2.98 頁/秒提升至 20.44 頁/秒
- 提供完整微調食譜，包含數據生成、NeMo Automodel SFT 和 NeMo RL GRPO，可應用於自訂文檔（如牙科表單）

## 結論
NVIDIA 透過開放數據集和提供完整微調食譜，降低開發者門檻，鼓勵社區擴展 Parse 模型對泰語、波斯語和阿拉伯語等語言的支持，並促進文檔解析應用開發。

---