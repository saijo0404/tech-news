# For Robotaxis: Safety Must Be Built In, Not Bolted On

- **來源**: NVIDIA Blogs
- **發布日期**: 2026-06-10
- **原文連結**: https://blogs.nvidia.com/blog/halos-os-robotaxi-safety/

## 核心主題
NVIDIA 宣布其全新 Halos 作業系統，作為 DRIVE Hyperion 平台的全堆疊安全基礎，透過認證 OS、標準化介面、AI 安全護欄與雲端驗證框架四大支柱，解決 Robotaxi 規模化部署中的安全性挑戰。

## 關鍵重點
- **Halos 作業系統四大核心組件**：（1）Halos Core——基於 DriveOS 新一代認證 OS，符合 ISO 26262 ASIL D 標準，透過 Hypervisor 隔離安全關鍵功能防止故障蔓延至車輛控制；（2）Halos SDK——傳感器抽象層與車輛抽象層實現硬體與軟體介面標準化，提供確定性排程器、零拷貝 IPC 與全面錯誤處理框架；（3）Halos Applications——以確定性、基於規則的函數為 AI 提供安全護欄，整合世界模型感知、主動安全系統（自動緊急煞車、車道偏離警告等），並支援 NVIDIA Alpamayo 開源模型的思維鏈推理；（4）Halos SEF 安全評估框架——結合 DGX 訓練、Omniverse/OVX 模擬與 AGX 車載即時處理，提供從 L2 到 L4 的完整安全驗證工具。
- **全球 Robotaxi 部署加速**：Uber 與 Autobrains 在慕尼黑部署、Foxconn 擴大與 NVIDIA 合作在臺灣部署、VinFast 在東南亞推出 L4 級別車輛、HUMAIN 將 DRIVE Hyperion 引入沙特阿拉伯，顯示 Robotaxi 正從原型階段邁入商業運營，安全基礎設施的必要性日益迫切。
- **從「事後附加」到「內建安全」的理念轉變**：NVIDIA 強調僅靠感知與決策不足以滿足監管要求——必須證明整體系統行為可靠、故障能在升級前隔離、且從不超出設計邊界運行；Halos OS 橫跨完整開發生命週期，將安全從附加功能轉為內建基礎，透過 330 篇研究論文與 1,000 項專利支撐安全主張。

## 結論
NVIDIA 以 Halos OS 回應 Robotaxi 產業從原型到商業化的關鍵安全痛點，透過認證作業系統、標準化介面、AI 安全護欄與雲端驗證的整合方案，確保自動駕駛車輛能在規模部署中維持安全可靠；隨著全球多個城市加速部署 Robotaxi，「安全必須內建而非事後附加」成為業界共識。

---
