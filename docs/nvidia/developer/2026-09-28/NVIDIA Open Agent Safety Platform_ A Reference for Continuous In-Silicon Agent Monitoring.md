# NVIDIA Open Agent Safety Platform: A Reference for Continuous In-Silicon Agent Monitoring

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-09-28
- **原文連結**: https://developer.nvidia.com/blog/nvidia-open-agent-safety-platform-a-reference-for-continuous-in-silicon-agent-monitoring/

## 核心主題
NVIDIA 推出開放式 AI 安全平台，透過軟體與硬體層疊架構，為 AI 代理提供持續的監控與安全強制機制。

## 關鍵重點
- **NVIDIA OpenShell**: 提供沙盒環境執行 AI 代理，具備核心級隔離能力，將操作員指令轉化為可驗證政策
- **NVIDIA Sentry**: 在 NVIDIA BlueField-4 DPU 硬體上擴展監控，透過 NVIDIA DOCA 進行帶外強制執行，提供實時政策強制
- **五項核心原則**: 可驗證政策、帶外強制執行、控制通往模型的途徑、可視化推理能力、共享責任模型
- **三層架構**: 應用層（模型、工具、數據）、運行時層（ orchestration 與監控）、基礎設施層（硬體資源）
- **Vera Rubin POD 架構**: BlueField-4 DPU 位於節點唯一通往模型的途徑上，提供持續監控與實時政策強制

## 結論
NVIDIA Open Agent Safety Platform 為 AI 代理生態系統提供信任基礎，透過軟體更新即可啟用，並與 NVIDIA Vera 系統及 BlueField-4 硬體整合，建立可持續演進的安全標準。

---