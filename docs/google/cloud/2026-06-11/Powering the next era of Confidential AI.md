# 打造保密 AI 新時代

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-11
- **原文連結**: https://cloud.google.com/blog/products/identity-security/powering-the-next-era-of-confidential-ai/

## 核心主題
Google Cloud 宣布與 Apple 合作，在 Google Cloud 基礎設施上擴展 Apple Private Cloud Compute（PCC），透過 Confidential Computing、Titanium 安全架構與 Intel TDX、NVIDIA Confidential Computing 的協同合作，為高安全性 AI 工作載量提供硬體層級的保密運算保障。

## 關鍵重點
- **Confidential Computing 保障資料在使用中加密**：基於 Google Titanium 安全架構與 Titan 晶片建立的硬體信任根，搭配 Intel TDX（Trust Domain Extensions）與 NVIDIA Confidential Computing，在硬體級別的可信執行環境（TEEs）中保護資料從靜態、傳輸中到使用中的全生命週期安全。
- **Apple PCC 在 Google Cloud 的多層安全設計**：Google Cloud 的 Confidential Computing 平台為 PCC 提供硬體隔離的虛擬機器，Titan 晶片確保開機流程與硬體平台的完整性，Intel CPU 與 NVIDIA Blackwell GPU 共同保護從 CPU 到 GPU 的完整運算路徑，並透過開源主機堆疊實現獨立驗證的安全性透明性。
- **跨廠牌協作树立保密 AI 標竿**：此合作整合了 Apple、Google Cloud、Intel 與 NVIDIA 四家的安全技術與標準，確保從硬體到軟體的每一層都貢獻於可驗證的安全系統，不僅服務 Apple PCC 的嚴格隱私標準，也將使所有 Google Cloud 客戶受益。

## 結論
Google Cloud 與 Apple 的 Confidential Computing 合作代表了雲端 AI 基礎設施在隱私保護上的重大里程碑，透過開源透明性、硬體信任根與跨廠牌技術整合，為處理敏感資料與 AI 工作載量的企業提供了可驗證、可審計的安全雲端平台。
