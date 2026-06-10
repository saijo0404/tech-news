# NVIDIA 提升 RTX 個人電腦與 DGX Spark 上的本地 AI 代理能力

- **來源**: NVIDIA Blog
- **發布日期**: 2026-05-31
- **原文連結**: https://blogs.nvidia.com/blog/rtx-ai-garage-computex-spark-local-agents/

## 核心主題
NVIDIA 在 GTC Taipei 宣布推出 RTX Spark 個人電腦與 DGX Station for Windows，搭配 OpenShell 安全執行環境與多項模型最佳化，將本地 AI 代理從開發者工具擴展至消費型電腦與企業桌面。

## 關鍵重點
- **RTX Spark 個人代理硬體與 OpenShell 安全整合**：RTX Spark 搭載 1 petaflops AI 運算與 128GB 統一記憶體，支援全天候電池續航；Microsoft 新安全原語與 NVIDIA OpenShell 提供沙盒化、隔離策略與個人資訊脫敏，Hermes Agent 與 OpenClaw 將整合至全新 Windows 應用程式。
- **llama.cpp 與 vLLM 多 GPU 效能提升**：透過多標記預測（MTP）與張量並行技術，llama.cpp 在 Qwen 3.6-27B 與 35B 上分別提升 2 倍與 1.6 倍推理速度；多 GPU 設置下記憶體增加 2 倍、運算提升 1.8 倍；vLLM 在 DGX Spark 上對 NVFP4 權重的 Qwen 3.6-35B 帶來 2.6 倍效能提升。
- **Adobe、H Company 與創意工具生態系擴展**：Adobe 將 Premiere 與 Photoshop 重新架構以運用 RTX Spark 統一記憶體與 TensorRT，AI 編輯與特效處理速度提升最高 2 倍；H Company 的電腦使用代理模型加速 2 倍、記憶體減少 35%；Blender 整合 DLSS 4.5 光線重建，NVIDIA Broadcast 2.2 推出 Studio Voice 功能。

## 結論
NVIDIA 透過 RTX Spark 硬體、OpenShell 安全層、模型最佳化與 Adobe 等夥伴生態系，將本地 AI 代理推入 Windows 消費型電腦與企業桌面，讓個人代理從開發者工具轉變為人人可用的數位夥伴。
