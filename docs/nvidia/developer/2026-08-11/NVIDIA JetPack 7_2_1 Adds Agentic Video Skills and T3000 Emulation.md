# NVIDIA JetPack 7.2.1 Adds Agentic Video Skills and T3000 Emulation

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-08-11
- **原文連結**: https://developer.nvidia.com/blog/nvidia-jetpack-7-2-1-adds-agentic-video-skills-and-t3000-emulation/

## 核心主題
NVIDIA JetPack 7.2.1 引入了代理式視頻技能 (agentic video skills) 和統一的 jetson-videosdk，使開發者能夠在視頻編碼 SDK 和 PyNvVideoCodec 之上構建可編程、設備感知的視頻工作流，並首次支持 PyNvVideoCodec 2.2。

## 關鍵重點
- **PyNvVideoCodec 2.2 支持**：首次為 Jetson 提供基於 Python 的硬體加速視頻編碼和解碼，利用 CUDA 設備緩衝區和 DLPack 協議實現與 AI 框架的無縫集成，包含多模式幀採樣和 ThreadedDecoder 等優化功能。
- **代理式視頻技能**：在 SDK 之上提供基礎視頻工作流技能，包括發現設備能力、生成編碼器配方、性能基準測試和驗證編碼工作流，將開發者的目標轉化為可重複的編碼工作流。
- **T3000 性能模擬**：在 Jetson T5000 模塊上模擬 Jetson T3000 的性能（865 FP4 TFLOPS），支持快速開發低功耗、高性能的 AI 視頻管道，適用於機器人和工作負載。

## 結論
JetPack 7.2.1 為開發者提供了從意圖到驗證的清晰路徑，通過統一的視頻技能層和 PyNvVideoCodec 2.2，使開發者能夠更輕鬆地構建和驗證 AI 視頻管道，同時未來版本將擴展更多技能以支持更廣泛的端到端應用。

---