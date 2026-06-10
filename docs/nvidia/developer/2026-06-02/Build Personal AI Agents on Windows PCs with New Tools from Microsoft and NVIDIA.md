# 使用 Microsoft 與 NVIDIA 新工具在 Windows PC 建構個人 AI 代理

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-02
- **原文連結**: https://developer.nvidia.com/blog/build-personal-ai-agents-on-windows-pcs-with-new-tools-from-microsoft-and-nvidia/

## 核心主題
NVIDIA 與 Microsoft 宣布一系列新工具，將 Microsoft eXecution Containers (MXC) 安全沙箱、NVIDIA OpenShell 執行環境、RTX Spark 硬體與 NemoClaw/Hermes Agent 整合於 Windows 平台，讓開發者在本地 PC 上安全、高效地建構與運行個人 AI 代理。

## 關鍵重點
- **Windows 本地代理安全與硬體生態**：Microsoft MXC 提供基於原生 Windows 機制的政策隔離層，NVIDIA OpenShell 整合 MXC 提供代理部署、政策管理、推論路由與 PII 遮蔽；RTX Spark 桌面與筆電提供 1 petaflop AI 運算、128GB 記憶體，Surface RTX Spark Dev Box 預載開發者專用 Windows 與工具包，OpenClaw 與 Hermes Agent 已率先採用 MXC/OpenShell 強化安全。
- **NemoClaw 擴展與模型效能提升**：NemoClaw 支援所有 NVIDIA 客戶端系統（GeForce RTX、RTX PRO、DGX Spark、DGX Station for Windows）並可運行 Hermes Agent；H Company 發布 Holo 3.1 模型（Computer Use 模式）以 FP8 量化節省 35% 記憶體，NVIDIA 優化後在 GPU 上實現 2 倍效能提升；llama.cpp 與 vLLM 透過 MTP 與 PDL 技術達成 Qwen 模型 2 倍推論效能。
- **多 GPU 加速與 Windows AI 平台成熟**：llama.cpp 支援張量平行（TP），雙 GPU 可達 ~2 倍記憶體與 ~1.8 倍運算效能；ComfyUI 整合 CFG 方法在雙 GPU 實現 2 倍運算；Windows AI Foundry 與 Windows ML API 全面 GPU 加速（Phi-Silica 3.3B 模型優先支援）；WSL-C 內建 Linux 容器支援讓開發者在 Windows 上直接執行專業級 Linux AI 環境。

## 結論
NVIDIA 與 Microsoft 透過安全沙箱、推論加速、多 GPU 擴展與 Windows AI 平台的深度整合，讓全球超過 1 億台 NVIDIA RTX PC 成為個人代理式 AI 的開發與運行基礎設施，大幅降低本地代理部署門檻。
