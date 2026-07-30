# Optimizing vLLM on Arm CPUs

- **來源**: vLLM Blog
- **發布日期**: 2026-07-29
- **原文連結**: https://vllm.ai/blog/2026-07-29-optimizing-vllm-on-arm-cpus

## 核心主題
vLLM 在 Arm CPU 上的性能優化與功能增強，包括記憶體分配、同步機制、密集層佈局、分頁注意力以及量化技術的改進。

## 關鍵重點
- **記憶體分配優化**：啟用 mimalloc 作為 PyTorch 預設記憶體分配器，Llama 3.1 8B 離線吞吐量提升 2.3 倍
- **高核心數同步優化**：利用 Arm LSE 原子指令優化 OpenMP 動態調度，TPOT 延遲降低 15%
- **密集層佈局優化**：啟用 oneDNN 快速路徑，BF16 權重預打包，TPOT 延遲降低 60%
- **分頁注意力優化**：使用 Arm BFMMLA 指令優化 QK/PV 路徑，分頁注意力速度提升 4 倍
- **量化優化**：INT8 W8A8 和 INT8 W4A8 量化技術，分別帶來 88% 和 29% 的吞吐量提升

## 結論
vLLM 在 Arm CPU 上的優化使服務吞吐量最高提升 6.2 倍，使 vLLM 成為更完善的生產級推理框架。
---
