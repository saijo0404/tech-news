---
# Boosting MoE Training Throughput with Advanced Fusion Kernels

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-15
- **原文連結**: https://developer.nvidia.com/blog/boosting-moe-training-throughput-with-advanced-fusion-kernels/

## 核心主題
NVIDIA 推出基於 CuTe DSL 打造的高階融合運算子（Fusion Kernels），解決 MoE 模型訓練中的記憶體與同步瓶頸，提供 1.3x–2x 的 Kernel 級加速，並支援無同步 CUDA Graph，在 DeepSeek-V3 與 GPT-OSS 訓練中分別帶來 8% 與 93% 的端到端效能提升。

## 關鍵重點
- **突破三大 MoE 訓練瓶頸**：傳統 MoE 訓練面臨三個主要問題——（1）啟用函數導致記憶體限制型 Kernel，使 Tensor Core 閒置；（2）CPU 排程瓶頸，Token 數需在執行時由 CPU 計算並觸發 Kernel 啟動；（3）量化成本，高轉低精度的量化操作同樣是記憶體限制型。NVIDIA 以自訂 Kernel 逐一解決。
- **CuTe DSL 融合 GEMM 與啟用函數**：針對 SwiGLU、GeGLU、sReLU 等 GLU 啟用函數，NVIDIA 重新包裝權重矩陣，使同一 thread block 能同時讀取輸入與閘道張量，在 GEMM epilogue 中直接完成 GLU 運算而無需寫入全域記憶體，同時原生支援偏差向量相加、特徵縮放與張量限制等融合操作。
- **無同步執行與低精度量化融合**：GroupGEMM Kernel 將每組 Token 數追蹤記錄於 GPU 記憶體中，消除 CPU 同步需求，實現完整迭代的 CUDA Graph；同時將 MXFP8 與 NVFP4 量化步驟融合進 GEMM Kernel 內，消除額外的 BF16 張量讀寫與 amax 計算記憶體通道。

## 結論
NVIDIA 的 CuTe DSL 融合 Kernel 已開放於 cuDNN Frontend（v1.23.0+）、Transformer Engine（v2.15+）與 Megatron Core（26.04-alpha.rc2+），開發者可依需求選擇不同抽象層級使用。隨著更多融合模式、JAX 支援與預先編譯（AOT）功能的持續開發，這套技術將為 MoE 模型訓練帶來更顯著的效能躍升。

---
