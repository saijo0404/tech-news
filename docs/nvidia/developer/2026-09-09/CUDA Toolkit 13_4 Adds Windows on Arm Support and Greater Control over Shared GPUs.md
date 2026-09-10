# CUDA Toolkit 13.4 Adds Windows on Arm Support and Greater Control over Shared GPUs

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-09-09
- **原文連結**: https://developer.nvidia.com/blog/cuda-toolkit-13-4-adds-windows-on-arm-support-and-greater-control-over-shared-gpus/

## 核心主題
CUDA Toolkit 13.4 新增 Windows on Arm 平台支援與 Rubin GPU 架構預覽功能，並帶來 GPU 資源管理與效能優化改進。

## 關鍵重點
- **Windows on Arm 支援**：擴展 CUDA 應用開發至 Windows on Arm 平台，不再限於 Linux on Arm，新增對 N1X Laptop 生態系支援。
- **Rubin GPU 架構預覽**：提供 compute capability 107 的預覽功能支援，開發者可提前移植應用。
- **GPU 資源管理改進**：Multi-Process Service V3 現代化 GPU 資源管理，具備可腳本化 CLI、命名伺服器實例、TOML 配置及 cgroup 整合的 GPU 記憶體限制。
- **CUDA Compute Fabric Transport**：提供跨 NVLink 傳輸的傳輸中心 API，支援命名邏輯終端點與異步操作。
- **CCCL 3.4 效能優化**：Blackwell GPU 上更快的 warp 專用 DeviceScan（記憶體頻寬利用率達 92%），支援 C++ 標準庫平行演算法。
- **開發者工具升級**：Nsight Python 1.0、Nsight Compute 2026.3、Nsight Systems 2026.5.1 等工具升級，支援自動化效能分析與跨平台開發。
- **cuBLAS 與 cuBLASLt 改進**：雙精度效能提升，支援固定點模擬，針對 MoE 工作負載優化。

## 結論
CUDA Toolkit 13.4 為開發者帶來更廣泛的平台支援（Windows on Arm、Rubin GPU）與更強大的 GPU 效能工具，同時提升 CCCL 與 cuBLAS 的效能表現，並強化開發者工具鏈的自動化與跨平台能力。
---