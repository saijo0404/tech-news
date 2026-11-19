# Keeping Agents Fast: High-Interactivity Decode with FlyDSL MonoKernels in vLLM

- **來源**: vLLM
- **發布日期**: 2026-11-18
- **原文連結**: https://vllm.ai/blog/2026-11-18-flydsl-monokernels

## 核心主題
vLLM 框架利用 FlyDSL MonoKernels 技術優化 AMD Instinct GPU 上的互動式 LLM 服務解碼延遲，透過將多個依賴操作階段合併到單一 GPU 核啟動中，大幅降低解碼延遲並提升用戶體驗。

## 關鍵重點
- **MonoKernel 技術核心**：將解碼層的多個依賴操作階段合併到單一 GPU 核啟動中，透過持久化啟動和重疊執行階段，大幅降低 GPU 核啟動/終止成本
- **性能提升顯著**：在 MI355X/MI325X 上，Concurrency-1 延遲提升 1.20× 至 2.26×；DeepSeek-V4.1-Flash 在 TP4 時 P90 互動性從 318.1 提升至 429.1 tok/s/user
- **支援模型廣泛**：已合併 DeepSeek-V4.1-Flash、DeepSeek-V4-Pro、MiniMax-M3、Kimi-K3、Muse Spark；審查中 GLM-5.x、Qwen3.8、MiniMax-M3.1
- **硬體支援**：支援 MI355X、MI325X、MI300X，並支援 MI300X/MI325X 的權重複製優化
- **使用方式**：透過 `--monokernel` 參數啟用，需設定 `VLLM_ROCM_USE_AITER = 1`，模型特定實現位於 `vllm/models/<model>/amd/`
- **限制與注意事項**：最佳於低並發（並發率 1 最佳），高並發時性能可能下降（並發率 4 時比兩台 TP4 還差 26%），步驟寬度有限制（DeepSeek-V4.1-Flash 48 行、MiniMax-M3/Kimi-K3 16 行）

## 結論
FlyDSL MonoKernels 為互動式 LLM 應用提供了顯著的性能提升，特別適合低並發場景。雖然需要手動啟用和特定硬體支援，但準確性測試顯示差異在噪音範圍內，所有配置均經過相同伺服器上的 mono 開/關比較驗證。

---
此摘要已儲存至指定檔案路徑。