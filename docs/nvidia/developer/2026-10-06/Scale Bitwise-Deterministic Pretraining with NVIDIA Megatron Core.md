# Scale Bitwise-Deterministic Pretraining with NVIDIA Megatron Core

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-10-06
- **原文連結**: https://developer.nvidia.com/blog/scale-bitwise-deterministic-pretraining-with-nvidia-megatron-core/

## 核心主題
本文介紹如何在大型模型預訓練中實現位元級確定性（bitwise determinism），並展示 NVIDIA Megatron Core 如何優化這種訓練方式。

## 關鍵重點
- **位元級確定性的價值**：允許可靠地重現失敗、調試損失尖峰、驗證系統變更以及從中斷的訓練恢復，對於 trillion-parameter 模型訓練至關重要。
- **優化成果**：通過在三個 Nemotron 工作負載上的優化，將確定性稅收降低至約 2%，同時在 2,432 張 GPU 上維持 800 步的位元級確定性。
- **關鍵核層優化**：如為分組 GEMM 寫入器提供私有輸出槽位並應用固定減少順序，在保持並行性的同時恢復了確定性結果。
- **驗證機制**：Megatron Core 通過配方驗證、核測試和模組驗證來防止回歸，涵蓋包括 FP8 和 FP4 在內的並行性配置。

## 結論
通過優化大型模型訓練的確定性，NVIDIA 可以減少 GPU 天數並提高訓練效率，同時確保訓練結果的可重複性和可調性。

---