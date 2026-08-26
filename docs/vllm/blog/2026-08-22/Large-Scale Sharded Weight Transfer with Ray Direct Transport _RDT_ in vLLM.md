# Large-Scale Sharded Weight Transfer with Ray Direct Transport (RDT) in vLLM

- **來源**: vLLM
- **發布日期**: 2026-08-22
- **原文連結**: https://vllm.ai/blog/2026-08-22-rdt-weight-transfer

## 核心主題
vLLM 推出大規模分塊權重轉移引擎，利用 Ray Direct Transport (RDT) 實現高效權重同步，支援密集、MoE 及量化模型。

## 關鍵重點
- **性能優化**：Kimi K2 模型在 48 台 8xH100 節點上，BF16 下僅需 7.53 秒，相比 NCCL broadcast 效率提升顯著（原需 64.72 秒）
- **通用性**：支援 dense、MoE（含融合/專家檢查點）及量化模型，框架只需描述權重佈局，引擎自動處理傳輸
- **故障容忍性**：基於 NIXL 後端，支援長訓練運行，可處理推理引擎失敗，失敗節點可在下次權重同步時重新加入
- **流水線執行優化**：V3 版本實現 gather/pull/replay 重疊，權重同步延遲從 5.61s 降至 3.49s

## 結論
vLLM 通過 RDT 技術實現了大規模模型權重轉移的顯著性能提升，為兆參以上開源模型和 RL 框架（如 SkyRL）提供了高效、通用且容錯的解決方案。

---