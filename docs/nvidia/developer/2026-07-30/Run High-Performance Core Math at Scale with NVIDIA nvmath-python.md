# Run High-Performance Core Math at Scale with NVIDIA nvmath-python

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-07-30
- **原文連結**: https://developer.nvidia.com/blog/run-high-performance-core-math-at-scale-with-nvidia-nvmath-python/

## 核心主題
本文介紹 NVIDIA nvmath-python 1.0 作為 Python 科學社群與 NVIDIA CUDA-X 數學庫之間的橋接層，提供高性能核心數學運算。

## 關鍵重點
- **跨平台支援**：支援 CPU、GPU 及分布式多節點系統，與 NumPy、CuPy、PyTorch 完美相容
- **彈性 API 設計**：提供通用 API 適合非效能關鍵任務，專用 API 針對特定硬體優化提供最高效能
- **自動調優功能**：根據硬體和工作負載自動選擇最佳核心，攤銷規劃與自動調優成本
- **FFT 功能整合**：支援 JIT 編譯的自訂前綴/後綴函數，提供 Gaussian 濾波等實例
- **Numba-CUDA 整合**：可從 Numba-CUDA 核函數中呼叫 nvmath-python 設備 API，支援幾何布朗運動等模擬應用

## 結論
nvmath-python 為開發者提供了高效、易用的核心數學運算解決方案，特別適合需要高性能計算的科學計算任務。透過自動調優和跨平台支援，大幅降低高性能計算的門檻。

---

安裝方式：pip install nvmath-python[cu13]

資源：提供 GitHub 倉庫、教學筆記、NVIDIA 加速計算培訓材料等資源。