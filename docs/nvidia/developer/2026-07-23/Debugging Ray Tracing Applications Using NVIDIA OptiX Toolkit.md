# Debugging Ray Tracing Applications Using NVIDIA OptiX Toolkit

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-07-23
- **原文連結**: https://developer.nvidia.com/blog/debugging-ray-tracing-applications-using-nvidia-optix-toolkit/

## 核心主題
這篇文章介紹了 NVIDIA OptiX Toolkit (OTK) 提供的兩種主要調試工具：統一的 API 錯誤檢查宏和針對性的設備端調試輸出機制，幫助開發者更有效地除錯 GPU 光線追蹤應用程序。

## 關鍵重點
- OTK 提供統一的錯誤檢查宏（OTK_ERROR_CHECK），可跨 OptiX、CUDA runtime 和 CUDA driver API 使用，自動生成包含來源位置、錯誤代碼名稱和人類可讀描述訊息的診斷訊息。
- DebugLocation 機制允許精確控制設備端調試輸出，支援單次調式匯出（one-shot mode）和視覺化調式標記，可與 ImGui 等 UI 框架整合。
- 文章包含 DemandPbrtScene 實例，展示了如何在 OptiX 管道中使用 DebugLocation 進行互動式調式輸出控制。

## 結論
NVIDIA OptiX Toolkit 為開發者提供了權宜的 BSD 3-clause 授權下的調式工具集，可顯著簡化 GPU 光線追蹤應用程序的開發和除錯過程。
---