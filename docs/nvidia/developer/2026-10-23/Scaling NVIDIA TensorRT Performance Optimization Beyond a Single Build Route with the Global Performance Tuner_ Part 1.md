# Scaling NVIDIA TensorRT Performance Optimization Beyond a Single Build Route with the Global Performance Tuner, Part 1

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-10-23
- **原文連結**: https://developer.nvidia.com/blog/scaling-nvidia-tensorrt-performance-optimization-beyond-a-single-build-route-with-the-global-performance-tuner-part-1/

## 核心主題
NVIDIA TensorRT 11.1 推出 Global Performance Tuner，解決傳統性能優化的擴展性問題，透過可自訂建置路徑和準確性感知優化來適應多樣化的模型和硬體平台。

## 關鍵重點
- 傳統 TensorRT 編譯器使用單一排程策略，無法適應所有模型，個別優化可能導致準確性問題或整體性能下降
- Global Performance Tuner 提供可自訂建置路徑，允許使用者定義不同的編譯路徑，擴展解決方案空間
- 準確性感知優化驗證每個候選方案是否符合端到端準確性要求，從更多候選方案中選擇最快且可接受的引擎
- 編譯過程建模為 Builder 算法（生成候選解決方案）與 Searching 算法（選擇最佳方案）的組合，理想情況下應包含全局最佳解

## 結論
此功能特別適用於處理多樣化的外部模型、硬體平台和應用需求，解決傳統基於內部 KPI 模型的優化工具擴展性不足的問題。此為系列文章第一部分，第二部分將介紹算法與架構設計細節。
