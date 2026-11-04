# Palette: teaching a small model to build decks in your design language

- **來源**: Hugging Face Blog
- **發布日期**: 2026-11-03
- **原文連結**: https://huggingface.co/blog/ibm-research/palette-deck-building

## 核心主題
IBM Research 開發了一個名為 Palette 的小型開源模型，通過訓練使其能夠根據 IBM Design Language 設計演示文稿，在保持內容所有權的同時與前沿系統競爭。

## 關鍵重點
- **分角色設計**：將幻燈片製作拆分為「設計師」（內容決策）和「程式碼」（幾何佈局）兩個角色，由單一 LoRA 適配器處理，大幅提升效率（6-7 倍）。
- **合成數據訓練**：使用反事實推理（解釋為什麼做出某個選擇而非其他）訓練模型，包含約 1000 套幻燈片、10,000 張幻燈片的數據。
- **檢查修復工具（Harness）**：自動檢查並修復錯誤幻燈片（重疊、溢出等），在 131 套演示文稿上平均提升 3.5 分。
- **用戶指令控制**：支持通過 [[ ]] 指令直接控制設計選擇（如 [[make this a timeline]]、[[be candid, no spin]] 等 12 類指令）。
- **評估表現**：在 PresentBench 評估中，經濟和教育領域排名第一，整體排名第二（59.7 分，僅次 NotebookLM 的 60.8 分）。

## 結論
Palette 證明小型開源模型可以通過分角色訓練、合成數據和檢查修復機制，在保持內容所有權的同時達到與前沿模型相當的表現，並能嚴格遵循特定設計語言。這為企業私有化部署和符合品牌規範的 AI 應用提供了可行路徑。
---
