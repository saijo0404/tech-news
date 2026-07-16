# Building Faster Cryptography with Carryless Multiplication in NVIDIA CUDA 13.3

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-07-15
- **原文連結**: https://developer.nvidia.com/blog/building-faster-cryptography-with-carryless-multiplication-in-nvidia-cuda-13-3/

## 核心主題
NVIDIA CUDA 13.3 引入硬體加速的無進位乘法累加指令（clmad），大幅提升 GPU 原生二進制擴展域運算效能，應用於 AES-GCM 認證加密與零知識證明等密碼學工作負載。

## 關鍵重點
- **GHASH 加速**：在 NVIDIA B200 上 GHASH 吞吐量達 6.3 TB/s，比 bitsliced 電路快 18.8 倍，接近 DRAM 讀取頻寬。
- **Sum-check 協議加速**：在 B200 上加速 4-13 倍，RTX 5090 上加速 3-4 倍，提升零知識證明系統效能。
- **硬體支援擴展**：clmad 指令支援 Ampere 架構（SM 80+）GPU，解決 GPU 原生二進制擴展域運算長期缺失問題。

## 結論
CUDA 13.3 透過硬體加速無進位乘法，顯著提升現代密碼學工作負載效能，特別適用於大規模認證加密與二進制域零知識證明，為開發者提供即插即用之 PTX 範例。
---