# Build Local AI Apps with C++ and NVIDIA TensorRT RTX Samples

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-10-01
- **原文連結**: https://developer.nvidia.com/blog/build-local-ai-apps-with-c-and-nvidia-tensorrt-rtx-samples/

## 核心主題
DIN Deploy 開放原始碼 C++ 樣本集合結合 ONNX Runtime 與 NVIDIA TensorRT RTX 執行提供者，加速本地 AI 推理應用。

## 關鍵重點
- 使用 Python 導出器將 Hugging Face 檢查點轉換為 ONNX 藝術品，再透過原生 C++ CLI 進行推理
- 支援自動語音識別（OpenAI Whisper、NVIDIA Parakeet TDT、NVIDIA Nemotron ASR Streaming）
- 支援互動式分割（Meta SAM 2.1）與提示驅動圖像生成（FLUX.2-klein-4B）
- GPU 加速性能顯著：Nemotron ASR 達 39x 實時、Parakeet TDT 達 206x、SAM 2.1 達 38.3 FPS

## 結論
DIN Deploy 提供跨平台（Windows/Linux）的本地 AI 應用解決方案，透過 CMake 預設配置簡化開發流程，並支援後訓練量化以進一步優化模型性能。

---