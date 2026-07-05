# Fine-Tuning Biological Foundation Models with LoRA Using NVIDIA BioNeMo Recipes

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-06-15
- **原文連結**: https://developer.nvidia.com/blog/fine-tuning-biological-foundation-models-with-lora-using-nvidia-bionemo-recipes/

## 核心主題
本文介紹如何透過 NVIDIA BioNeMo Recipes，以 LoRA（低秩適配）技術在單張工作站 GPU 上高效微調數十億參數級的生物基礎模型（蛋白質模型 ESM2-3B 與 DNA 模型 Evo2-1B），展現參數高效微調的強大潛力。

## 關鍵重點
- **LoRA 技術原理與成效**：LoRA 凍結預訓練主幹模型，僅訓練約 1% 的低秩適配矩陣，大幅降低運算與記憶體需求。ESM2-3B 微調後在蛋白質二級結構預測（PSSP）中達到 Q3 準確率 84.80%、Q8 準確率 74.30%，與 Porter 6 等最先進基線相當；Evo2-1B 在 DNA 剪接位點分類中，僅訓練 1.42% 參數即可將準確率從 52.3% 提升至 96.6%。
- **效能優化關鍵技術**：BioNeMo Recipes 整合 Transformer Engine（TE）加速、Megatron-Bridge 分散式訓練、以及序列打包（THD 格式），將吞吐量提升 5.5 倍並減少記憶體使用，使單張 NVIDIA RTX 6000 Blackwell 能在不到一小時內完成完整訓練。
- **跨模態適用性與開放工具鏈**：相同的 LoRA 配方同時適用於蛋白質（Transformer 架構）與 DNA（Hyena 混合架構）等不同生物模態。BioNeMo Recipes 將高效訓練堆疊設為預設整合，提供基於 PyTorch 和 Hugging Face 的一站式範例，搭配 PEFT 庫與完整的 CLI 訓練指令，降低使用者自組流程的門檻。

## 結論
NVIDIA BioNeMo Recipes 證明數十億參數的生物基礎模型如今可在適度硬體上進行高效微調。透過 LoRA 的參數高效策略搭配完善的效能優化工具鏈，研究人員能以極低資源門檻獲得與全量微調相當的精度，為生物資訊與藥物開發領域帶來更親民的 AI 研究途徑。

---
