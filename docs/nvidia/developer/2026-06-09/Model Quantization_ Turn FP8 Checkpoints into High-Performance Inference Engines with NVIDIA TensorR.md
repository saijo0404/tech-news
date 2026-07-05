# Model Quantization: Turn FP8 Checkpoints into High-Performance Inference Engines with NVIDIA TensorRT

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-09
- **原文連結**: https://developer.nvidia.com/blog/model-quantization-turn-fp8-checkpoints-into-high-performance-inference-engines-with-nvidia-tensorrt/

## 核心主題
NVIDIA 示範如何將 FP8 量化模型 checkpoint 透過 Model Optimizer 與 TensorRT 轉化為高效能推論引擎，在 CLIP 模型上實現高達 1.45 倍的加速與近半的記憶體佔用降低。

## 關鍵重點
- **從 ModelOpt 到 TensorRT 的完整部署流程**：將 FP8 checkpoint 匯出為 ONNX 格式（文字編譯器檔案縮小約 34%、影像編譯器縮小約 50%），透過 trtexec 建置 TensorRT 引擎，過程中 Q/DQ（量化/反量化）節點會在引擎建置階段被融合為專用的 FP8 核心，消除不必要的精度轉換開銷。
- **實測效能提升顯著**：在 NVIDIA RTX 6000 Ada GPU 上，影像編譯器延遲從 166.2 ms 降至 119.8 ms（1.39 倍加速），文字編譯器從 13.2 ms 降至 9.1 ms（1.45 倍加速）；GEMM 運算從約 1.8 ms 降至 0.84 ms，TensorRT 引擎總體積縮小近一半，大幅降低 VRAM 需求。
- **TensorRT 量化機制的深度剖析**：TensorRT 在引擎建置時會尋找 ONNX 中的 QuantizeLinear/DequantizeLinear 節點，將其與相鄰層融合並替換為專用的低精度核心，讓量化後的權重與激活值直接在 FP8 Tensor Cores 上執行，獲得更高的運算吞吐量與更低的記憶體頻寬需求。

## 結論
NVIDIA 提供了一套從量化、匯出、建置到基準測試的完整工具鏈（Model Optimizer + TensorRT + Nsight Deep Learning Designer），讓開發者能將 FP8 量化模型快速部署為生產級推論引擎，在幾乎不犧牲準確度的前提下獲得顯著的效能與資源節省。

---
