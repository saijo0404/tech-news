---
# NVIDIA Vera CPU 在競爭中打出重拳

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-05-26
- **原文連結**: https://blogs.nvidia.com/blog/vera-cpu-phoronix/

## 核心主題
NVIDIA Vera CPU 透過自製 Olympus 核心與 LPDDR5X 記憶體子系统，在 Phoronix 測試中展現超越 Intel/AMD x86_64 處理器的性能，成為 AI 代理工作負載的理想選擇。

## 關鍵重點
- **88 個 NVIDIA Olympus 核心**：支援 Armv9.2 指令集，專為 AI 代理工作負載設計（分支密集型運算、沙盒程式、數據處理與調度），單晶片整合 1.2TB/s 記憶體頻寬與高速片上總線，450W TDP 下展現卓越效能。
- **記憶體性能突破**：採用第二代 LPDDR5X 記憶體子系统，功耗低於 30W 即提供 1.2TB/s 頻寬（傳統 CPU 需超過 100W），在 Phoronix STREAM TRIAD 測試中維持 90% 峰值頻寬，單核記憶體頻寬是傳統 x86 CPU 的 4 倍以上。
- **代際性能躍升**：相較於前代 Grace CPU，Vera 在 Phoronix 測試中實現 1.6 倍的幾何平均性能提升；整體性能比最新 128 核 x86 處理器高出 1.5 倍，單核基準比 AMD EPYC 9575F 高出 10%，Linux 核編譯速度快達 20 秒（單晶片）。

## 結論
NVIDIA Vera CPU 透過自製核心與高效記憶體子系统，在 AI 代理工作負載上展現超越業界現有 ARM/x86 處理器的性能，並已交付給首批 AI 公司與雲端供應商，預計於 2026 年下半年與夥伴共同推出。
