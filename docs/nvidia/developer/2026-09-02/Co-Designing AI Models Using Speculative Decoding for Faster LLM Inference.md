# Co-Designing AI Models Using Speculative Decoding for Faster LLM Inference

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-09-02
- **原文連結**: https://developer.nvidia.com/blog/co-designing-ai-models-using-speculative-decoding-for-faster-llm-inference/

## 核心主題
本文介紹使用 Speculative Decoding 加速 LLM 推理的方法，透過小型 draft model 預測多個 token 並由大型 target model 並行驗證，減少解碼迭代次數。

## 關鍵重點
- **五個關鍵指導原則**：將 GEMM 推入計算密集型區域、當注意力佔比高時設定 draft length = 128/G - 1、根據 draft length 調整、極低延遲時的 acceptance 收益考量、平衡 acceptance length 與 draft overhead
- **主要 draft mechanism 比較**：EAGLE-3、DFlash、DSpark 使用輔助層適合 GPU；外部 draft model 訓練成本最高適合 LPU；Suffix/n-gram 無需訓練適合高重複模式
- **工具與資源**：NVIDIA SPEED-Bench 用於測量 acceptance length；NVIDIA/Model-Optimizer 提供訓練示例與量化工作流
- **Draft 機制選擇**：DFlash 和 DSpark 在低延遲場景下表現優異，即使 AL 較低，因 draft 延遲較低，適合小模型
- **性能評估**：建議使用 SPEED-Bench 測量 AL，以 NVIDIA TensorRT LLM 量化 draft overhead
- **訓練成本考量**：MTP 需與目標模型共訓練，EAGLE、DFlash、DSpark 可加入最終檢查點，訓練成本較低
- **目標模型變更**：針對式 draft 器需隨目標模型更新而重新訓練，外部 draft 模型則需微調
- **實作建議**：選擇 draft 機制時應平衡 AL、draft 延遲與訓練/部署成本；建議 draft 長度 D = 128/G - 1 作為起始點

## 結論
透過合理選擇 draft length 和 draft mechanism，並使用 NVIDIA 提供的工具如 SPEED-Bench 和 Model-Optimizer，可以有效加速 LLM 推理同時保持準確性。
---