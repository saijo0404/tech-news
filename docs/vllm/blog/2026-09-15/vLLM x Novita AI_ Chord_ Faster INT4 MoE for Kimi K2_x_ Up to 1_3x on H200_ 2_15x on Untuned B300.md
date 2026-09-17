# vLLM x Novita AI: Chord, Faster INT4 MoE for Kimi K2.x. Up to 1.3x on H200, 2.15x on Untuned B300

- **來源**: vLLM Blog
- **發布日期**: 2026-09-15
- **原文連結**: https://vllm.ai/blog/2026-09-15-novita-chord-w4a16-moe

## 核心主題
Novita AI 開源了 Chord，一個針對 Kimi K2.x 架構的高性能 W4A16 MoE CUDA 算子，相比 Humming 在特定硬體上可獲得 1.1x 至 2.15x 的性能提升。

## 關鍵重點
- **H200 EP8 prefill**：相比 Humming 提升 1.11–1.20x，採用 batched wait<1> WGMMA 流水線技術
- **H200 TP8 單實例服務**：提升 1.17–1.33x，支援 H200 EP8 prefill、H200 TP8 單實例服務、H200 EP8 decode 及 B200/B300 EP8 decode
- **H200 EP8 decode**：提升 1.16–1.24x，down stage 可達 1.31x，採用 barrier-bound 的 WGMMA 路徑
- **B300 EP8 decode**：提升 1.81–2.15x（對比 Humming 預設未優化配置），因 Humming 未提供 SM100/SM103 調優表
- **兩種核種實現**：提供 indexed（Humming 衍生）和 grouped（DeepGEMM 衍生）兩種獨立實現，支援 uint4、group-32、BF16 scales

## 結論
Chord 透過針對 Kimi K2.x 架構的專用優化，在 H200 和 B300 等硬體上實現顯著性能提升，特別是在未優化的 B300 上可達 2.15x 加速。使用者可透過 `--quantization humming` 參數在 vLLM 中啟用，但需注意 grouped 整合仍在開發中。

---