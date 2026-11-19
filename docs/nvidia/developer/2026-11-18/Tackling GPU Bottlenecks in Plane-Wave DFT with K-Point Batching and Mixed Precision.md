# Tackling GPU Bottlenecks in Plane-Wave DFT with K-Point Batching and Mixed Precision

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-11-18
- **原文連結**: https://developer.nvidia.com/blog/tackling-gpu-bottlenecks-in-plane-wave-dft-with-k-point-batching-and-mixed-precision/

## 核心主題
NVIDIA 推出 Daviator 庫與混合精度技術，解決平面波 DFT 中的 GPU 瓶頸，大幅提升計算效率並降低成本。

## 關鍵重點
- **性能提升**：Daviator 透過 K-point batching 與混合精度技術，使 VASP 計算比 CPU 快最多 22 倍，成本降低最多 75%
- **技術核心**：使用批處理 Davidson 本徵值求解器，混合精度執行層採用 FP32 運算 + FP64 儲存關鍵部分
- **部署方式**：透過 NVIDIA ALCHEMI VASP microservice 即可啟用，設定 LDAVIATOR=True 即可，無需額外授權
- **效能比較**：在 RTX PRO 6000 等高 FP32:FP64 比率 GPU 上，FP32 Daviator 比 FP64 快 3-7 倍，端到端加速約 2 倍
- **成本節省**：混合精度可節省高達 $200,000，對於 OMat24 規模數據集，可節省 60-75% 成本（約 $5-6M）

## 結論
NVIDIA 透過 Daviator 庫與混合精度技術，成功解決了平面波 DFT 計算中的 GPU 瓶頸問題，使小系統計算也能高效利用 GPU 資源，大幅降低計算成本。
---
