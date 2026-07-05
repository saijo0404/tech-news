# Creating the NVIDIA Nemotron 3 Ultra NVFP4 Checkpoint with NVIDIA Model Optimizer

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-26
- **原文連結**: https://developer.nvidia.com/blog/creating-the-nvidia-nemotron-3-ultra-nvfp4-checkpoint-with-nvidia-model-optimizer/

## 核心主題
NVIDIA Model Optimizer 0.46 推出 NVFP4 Four-Over-Six 量化技術，並提供 Nemotron 3 Ultra 550B 參數模型的完整混合精度量化配方，讓開發者能透過 YAML 自訂組態或一鍵啟動器，將大型語言模型量化為高效能推理checkpoint。

## 關鍵重點
- **NVFP4 Four-Over-Six 權重量化技術**：Four-Over-Six（4/6）僅套用至權重層，激活值回傳至預設 NVFP4。其核心為 4/6 自適應區塊縮放（adaptive block scaling），在權重上使用 E2M1 格式、16 寬區塊與 E4M3 比例尺，透過 amax 乘數調整（M=6 保留原始 amax，M=4 以 amax×6/4 縮放）最佳化量化精度，在推理效率與模型準確性之間取得平衡。
- **高度客製化的混合精度 YAML 配方**：Model Optimizer 提供多種內建預設組態（NVFP4_DEFAULT_CFG、NVFP4_MLP_ONLY_CFG、NVFP4_EXPERTS_ONLY_CFG 等），並支援使用者撰寫完整 YAML 配方精確控制每個模組的量化層級。Nemotron 3 Ultra 範例配方將路由專家權重設為 NVFP4 W4A4、共享專家與 Mamba 投影設為 FP8、KV 快取設為 FP8，其餘維持 BF16，展現對 MoE 架構中不同元件的細粒度控制能力。
- **通用量化流程與一鍵部署**：量化流程適用於任何 Hugging Face 模型，只需使用 `mtq.quantize()` 搭配選擇的組態，再以 `export_hf_checkpoint()` 匯出供 TRT-LLM、vLLM、SGLang 使用的統一 checkpoint。Model Optimizer 一鍵啟動器（launch.py）更將整個 Ultra PTQ 與匯出流程自動化，驗證於四節點各配備四張 NVIDIA Blackwell GPU 的 Slurm 叢集環境。

## 結論
NVFP4 Four-Over-Six 與 YAML 配方系統將 NVIDIA Model Optimizer 的量化能力提升至新的層級——從通用預設組態到針對 MoE 架構的細粒度混合精度設定，開發者能針對路由專家、共享專家與 Mamba 投影等元件選擇最適合的精度。透過一鍵啟動器與通用流程，從 PTQ 量化到推理部署的整個鏈結變得更加高效直觀，為 500B 級大模型的生產級低精度推理鋪平了道路。

---
