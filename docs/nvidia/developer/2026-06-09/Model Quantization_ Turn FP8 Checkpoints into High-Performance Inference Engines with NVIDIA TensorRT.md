# 模型量化：使用 NVIDIA TensorRT 將 FP8 權重轉換為高效能推理引擎

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-09
- **原文連結**: https://developer.nvidia.com/blog/model-quantization-turn-fp8-checkpoints-into-high-performance-inference-engines-with-nvidia-tensorrt/

## 核心主題
本文展示如何將 NVIDIA Model Optimizer 產出的 FP8 量化 CLIP 模型導出為 ONNX 格式，並編譯為 NVIDIA TensorRT 推理引擎，在生產環境中實現更快的推理速度、更高的吞吐量和更有效的 GPU 資源利用率。

## 關鍵重點
- **從 ModelOpt 到 ONNX 的完整流程**：使用 ModelOpt 將 FP8 量化的 CLIP 模型導出為 ONNX（opset 20+），文字編譯器模型檔案縮小約 34%，影像編譯器縮小約 50%，TensorRT 在引擎建置時會將量化節點與權重融合，進一步最佳化效能。
- **FP8 帶來顯著的速度與記憶體提升**：在 NVIDIA RTX 6000 Ada GPU 上的實測顯示，FP8 TensorRT 引擎較 FP16 基線而言，影像編譯器推理延遲降低至 119.8ms（1.39 倍加速）、文字編譯器降至 9.1ms（1.45 倍加速），整體引擎體積縮減近半，GPU VRAM 需求同步下降。
- **TensorRT 的量化核心機制**：TensorRT 在引擎建置階段會識別 ONNX 圖中的 QuantizeLinear/DequantizeLinear（Q/DQ）節點，並將其融合至相鄰圖層，替換為專屬的低精度運算核心（FP8 Tensor Core），消除不必要的量測往返開銷，從而提升運算吞吐量並降低記憶體頻寬消耗。

## 結論
透過 ModelOpt 與 TensorRT 的協同作業，開發者可以輕鬆將 FP8 量化模型部署為高效能生產推理引擎，在維持模型品質的同時，獲得顯著的速度加速與記憶體節省，為大規模 AI 推理應用提供實用的效能優化路徑。
