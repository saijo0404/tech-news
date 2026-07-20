# Fine-tune video and image models at scale with NVIDIA NeMo Automodel and 🤗 Diffusers

- **來源**: Hugging Face Blog
- **發布日期**: 2026-07-17
- **原文連結**: https://huggingface.co/blog/nvidia/scale-diffusers-finetuning-nemo-automodel

## 核心主題
NVIDIA 與 Hugging Face 合作推出 NeMo Automodel，讓使用者能輕鬆對支援的擴散模型進行大規模微調，無需轉換檢查點或修改模型代碼。

## 關鍵重點
- **無需檢查點轉換**：預訓練權重可直接使用，微調後的檢查點能直接載入 DiffusionPipeline 進行推理，或重新上傳至 Hugging Face Hub。
- **支援多模型**：支援 Wan 2.1/2.2、FLUX.1-dev/2-dev、HunyuanVideo、Qwen-Image 等主流擴散模型。
- **可擴展訓練**：支援 FSDP2、tensor parallel、expert parallel、context parallel 和 pipeline parallel 等多種並行策略，可從單卡擴展至數百張 GPU。
- **完整與 LoRA 微調**：支援完整微調（最大品質）和 LoRA 風格的 PEFT（最大效率），同一套 recipe 結構可處理兩種方式。
- **性能優異**：在 8×H100 GPU 上訓練 FLUX.1-dev 僅需 0.9 秒/步驟，支援多解析度桶裝資料載入以加速吞吐量。

## 結論
NeMo Automodel 為擴散模型微調提供了簡單、高效且可擴展的解決方案，特別適合需要大規模訓練的場景。使用者只需指向 Hugging Face Hub 上的模型 ID 即可開始訓練，無需額外的轉換步驟或模型重寫。

---