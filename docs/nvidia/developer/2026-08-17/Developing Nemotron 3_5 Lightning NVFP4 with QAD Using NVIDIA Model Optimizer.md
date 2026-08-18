# Developing Nemotron 3.5 Lightning NVFP4 with QAD Using NVIDIA Model Optimizer

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-08-17
- **原文連結**: https://developer.nvidia.com/blog/developing-nemotron-3-5-lightning-nvfp4-with-qad-using-nvidia-model-optimizer/

## 核心主題
本文介紹使用 NVIDIA Model Optimizer 的 QAD 技術，將 Nemotron 3.5 Lightning 模型從 66GB 壓縮至 22GB，實現 4 倍吞吐量提升，同時保持接近 BF16 基準的準確性。

## 關鍵重點
- **QAD 兩階段流程**：PTQ (Post-Training Quantization) 對全精度教師模型進行量化，生成 W4A16/NVFP4 學生檢查點；QAD (Quantization-Aware Distillation) 使用 KL 散度損失，在靜止的 BF16 教師模型上訓練學生模型，恢復量化造成的準確性損失。
- **激進量化策略**：採用更激進的 W4A16 量化（而非保守的 FP8），以最大化記憶體與延遲收益。量化策略分為動態比例 QAD（源自 max-calibrated 檢查點）和靜止比例 QAD（源自 MSE-based 檢查點）。
- **實驗驗證結果**：QAD 在準確性恢復上優於 PTQ 單獨使用，在代理與編碼基準測試中表現更優。所有檢查點均為 21.19GB，與 BF16 基準 65.85GB 相比大幅壓縮。
- **可複製性工作流**：提供完整訓練工作流，包含 recipe 選擇、訓練配置與檢查點導出，支援 Hugging Face 模型量化範例。

## 結論
QAD 使激進量化成為可能，在大幅降低記憶體佔用的同時保持接近原始模型的精度，特別適合精密度要求高的場景。通過 NVIDIA Model Optimizer 的 `megatron_lm_qad.yaml` 或 `mbridge_qad.yaml` launcher 可一鍵運行三步流程：量化 BF16 教師生成分生、對靜態教師進行精化、導出可部署檢查點。

---