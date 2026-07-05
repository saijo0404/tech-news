# Beyond LoRA: Can you beat the most popular fine-tuning technique?

- **來源**: HuggingFace Blog
- **發布日期**: 2026-06-18
- **原文連結**: https://huggingface.co/blog/peft-beyond-lora

## 核心主題
Hugging Face 發布 PEFT 基準測試，針對「為何 LoRA 幾乎是微調的唯一選擇」提出質疑，透過統一樣本與公平比較，證實 LoRA 雖表現良好，但並非在所有場景下都是最佳選擇，且切換 PEFT 技術僅需修改一行程式碼。

## 關鍵重點
- **LoRA 的統治地位與研究偏差**：在 Hugging Face Hub 上，98.4% 提及 PEFT 技術的模型卡使用 LoRA；GitHub 搜尋結果中 LoRA 佔 71.3%。作者指出這種壟斷可能來自自我強化效應（最多教程、最多人使用），而非 LoRA 在所有場景下真的最好。此外，研究論文常因壓力和不同實驗設定導致結果難以公平比較與重現。
- **公平基準測試結果**：Hugging Face 在相同基礎模型、數據集、訓練代碼與硬體下比較多個 PEFT 技術。在 LLM 數學推理（MetaMathQA/GSM8K）上，LoRA 達 53.2% 準確率需 22.6 GB VRAM；但 Lily 以 25.6 GB 達 54.9%，BEFT 以 20.2 GB 達 32.9%，且不同 LoRA 變體（如 LoRA-FA、rs-LoRA）表現差異顯著。在影像生成基準中，OFT 以更低記憶體（9.01 GB vs 9.97 GB）和更高相似度（0.708 vs 0.697）嚴格超越 LoRA。
- **實用考量與生態系支援**：除性能外，還需考量執行時間、檢查點大小、量化支援與層類型限制。雖然 vLLM 等下游套件目前僅支援 LoRA，PEFT 已提供將其他適配器轉換為 LoRA 的功能（轉換後測試分數幾乎無損，相似度 0.702→0.694）。切換技術僅需更改一處配置：`LoraConfig` 換成 `OFTConfig` 或 `GraLoRA` 等。

## 結論
LoRA 絕對不是壞選擇，但絕不該是自動預設值。Hugging Face 透過開放基準與統一 API 證明，在影像生成等場景中，其他 PEFT 技術已能超越 LoRA。使用者應根據自身需求（記憶體、準確率、生態系相容性）評估多項技術，即使偏好 LoRA，也值得嘗試其變體（DoRA、rs-LoRA、LoRA-FA）——因為微調的選擇權，不應被單一技術綁架。

---
