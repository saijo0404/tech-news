# How DOCA GPUNetIO Unifies GPU-Initiated Networking Across the NVIDIA Software Stack

- **來源**: developer.nvidia.com/blog
- **發布日期**: 2026-10-06
- **原文連結**: https://developer.nvidia.com/blog/doca-gpunetio-gda-ki-unified-gpu-networking/

## 核心主題
DOCA GPUNetIO 提供統一的 GDA-KI 基礎架構，讓 CUDA 核可直接驅動 Ethernet、RDMA、Verbs 和 DMA 操作，將 CPU 排除在應用關鍵路徑之外。

## 關鍵重點
- 提供完整的 DOCA SDK 超集與輕量開源 Verbs 實現，支援 NCCL、NVSHMEM、UCX/NIXL、Holoscan Sensor Bridge 等多個通訊庫
- 統一 GDA-KI 實現，減少重複開發與碎片化，降低實現複雜度
- 移除 CPU 瓶頸，資料路徑完全由 GPU 執行，小訊息頻寬提升
- 最小化延遲（如 NVQLink 達 2.6 微秒），使用 B300+CX8 平台測試驗證
- 整合通用功能，減少重複實現，降低維護成本

## 結論
DOCA GPUNetIO 透過 GPU 驅動式通訊抽象層，整合 GDA-KI 技術，顯著降低實現複雜度並提升通訊效能，是 NVIDIA 軟體堆疊中 GPU 網路架構的重要進展。
---