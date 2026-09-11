# High-Throughput Structure Prediction with BioNeMo Inference Runtime

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-09-10
- **原文連結**: https://developer.nvidia.com/blog/high-throughput-structure-prediction-with-bionemo-inference-runtime/

## 核心主題
NVIDIA BioNeMo Inference Runtime (BioIR) 加速支援的生物分子結構預測模型在 NVIDIA GPU 上的執行，同時保留熟悉的 PyTorch 工作流。

## 關鍵重點
- **端到端處理器**：BioIR 提供完整的端到端處理器，將輸入通過解析、分詞、特徵生成、GPU 推理和 PDB/mmCIF 輸出，並支援直接 PyTorch 模組整合。
- **Ray 執行器**：對於大型工作列表，Ray 執行器在單一節點上的每個 GPU 上放置完整的模型副本，透過重疊 CPU 階段與 GPU 摺疊來提高吞吐量。
- **性能提升**：在 1,000 個人類二聚體目標的比對測試中，BioIR 加速的 Boltz-2 模型每分配 GPU 小時成功摺合 58.5K 殘基，相比開源實現的 20.2K 提升 2.90 倍。
- **三層優化**：BioIR 優化在三個層面運作：核選取、模組優化（使用 CUDA Graph 捕捉）以及透過 Ray 副本的管道縮放。
- **能量效率**：估計摺合一百万個可比目標的評定功率等效能量，BioIR 為 11 MWh，而使用 8-GPU TDP 等效值的公共實現為 35 MWh。

## 結論
BioNeMo Inference Runtime 為大規模生物分子結構預測工作提供加速解決方案，已應用於 AlphaFold Database 擴展等實際案例，可顯著提升蛋白質複合物結構的生成效率。

---