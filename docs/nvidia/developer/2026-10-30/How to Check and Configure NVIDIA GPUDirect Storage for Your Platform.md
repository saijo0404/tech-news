# How to Check and Configure NVIDIA GPUDirect Storage for Your Platform

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-10-30
- **原文連結**: https://developer.nvidia.com/blog/how-to-check-and-configure-nvidia-gpudirect-storage-for-your-platform/

## 核心主題
本文介紹了 gds-diag 工具，這是一個開源命令行工具，可用於評估 NVIDIA GPUDirect Storage (GDS) 環境，並提供可選的 AI 代理技能以簡化診斷流程。

## 關鍵重點
- gds-diag 是一個開源命令行工具，提供多種診斷子命令，涵蓋端到端檢查、安裝前驗證、安裝後驗證和深度診斷
- 可選的 AI 代理技能提供自然語言介面，可自動選擇適當的診斷子命令並協調多步驟診斷工作流程
- 診斷結果以狀態徽章形式呈現（FAIL/WARN/INFO/PASS），每個發現都包含解釋和緩解計劃
- 工具可通過 NVIDIA Magnum IO GitHub 倉庫下載，需要 Linux 系統和 Python 3.8 或更高版本

## 結論
gds-diag 工具為管理人員提供了簡化 GPUDirect Storage 配置和優化的方法，通過命令行介面或 AI 代理技能兩種方式使用，可幫助識別問題並提出改進建議。
---