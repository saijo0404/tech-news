---
# For Robotaxis, Safety Must Be Built In, Not Bolted On

- **來源**: NVIDIA Blog
- **發布日期**: 2026-06-10
- **原文連結**: https://blogs.nvidia.com/blog/halos-os-robotaxi-safety/

## 核心主題
NVIDIA 介紹全新推出的 Halos Operating System，一套從底層架構深度建構的完整自動駕駛安全系統，強調機器人計程車的安全性必須內建於系統設計之中，而非事後添加。

## 關鍵重點
- **Halos Core — 安全認證作業系統**：作為 DriveOS 的下一代，透過 ISO 26262 ASIL D 認證，內建 Hypervisor 隔離安全關鍵功能，確保故障無法影響車輛控制，並支援 TensorRT Edge-LLM 進行大型語言模型推論。
- **Halos SDK — 標準化安全介面**：提供感測器抽象層與車輛抽象層，解耦自動駕駛堆疊與個別感測器驅動程式，內建確定性排程器、零拷貝通訊與完整錯誤處理框架，降低整合複雜度並確保低延遲。
- **Halos Applications — AI 安全防護**：透過確定性規則基礎函數為 AI 模型提供安全防護網，包含世界模型感知與 NVIDIA 獲獎的 DRIVE 主動安全套件（如自動緊急煞車、車道偏離警告、盲點監控），並支援可解釋的端到端 AI 模型。
- **Halos Infra — 雲端驗證基礎設施**：整合 DGX 訓練、Omniverse 模擬與 AGX 車載電腦，搭配 Halos 安全評估框架（SEF），支援從 L2 到 L4 的完整安全案例建構，涵蓋超過 330 篇研究論文與 1,000 項專利。

## 結論
NVIDIA 透過 Halos 全stack 安全系統，為機器人計程車提供從作業系統、介面、AI 防護到雲端驗證的一體化解決方案，並已在慕尼黑、台灣、東南亞、沙烏地阿拉伯等地推動全球部署，展現其對安全至上的堅持。

---
