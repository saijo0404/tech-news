---
# Inside NVIDIA Halos for Robotics: A Full-Stack Functional Safety System for Physical AI

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-06-22
- **原文連結**: https://developer.nvidia.com/blog/inside-nvidia-halos-for-robotics-a-full-stack-functional-safety-system-for-physical-ai/

## 核心主題
NVIDIA 推出 Halos for Robotics——將自動駕駛領域超過 18,000 年工程經驗與 210 億個安全晶體管的驗證基礎延伸至工業機器人、人型機器人与 AMR，打造涵蓋硬體安全島、認證作業系統到第三方檢驗認證的端到端完整功能安全平台。

## 關鍵重點
- **IGX Thor 硬體安全與 HSB 感測器延伸**：IGX Thor 整合 IEC 61508 SIL 3 認證的 Safety Island（獨立 I/O、電源、時鐘）、超過 22,000 個安全機制的高診斷覆蓋率、多樣化冗餘架構與防止干擾（FFI）支援；Holoscan Sensor Bridge（HSB）透過 Ethernet 連接感測器與執行器，支援 RDMA 低延遲串流、MACsec 加密認證與端到端 IEC 61508 SIL 2 安全通訊，將安全鏈延伸至感測器端。
- **Halos OS 軟體安全環境與 Outside-In 藍圖**：Halos Core 提供 Linux 與 Linux+QNX（NV Hypervisor 隔離 AI 與安全關鍵功能）兩種組態；Outside-In Safety Blueprint 利用外部設施攝影機擴展機器人感知，包含 SIPP（感知管線）、SAIM（監控 AI 模型異常並觸發安全狀態）、SEI（融合多攝影機事件）與 SDM（安全島上執行有限狀態機）。自動化貨櫃裝載（ATL）實例證明：當叉車在貨櫃內且無人員時，SDM 可暫時解除本體安全以提升效率，人員進入時立即恢復，使安全性與生產力不再衝突。
- **Halos AI Systems Inspection Lab 與開發者工具**：NVIDIA 建立全球首個同時涵蓋自動駕駛與機器人領域、獲 ANAB 認證的 ISO/IEC 17020 檢驗機構，提供從 IGX SoM、Halos Core 到應用程式的預評估路徑，夥伴憑 NVIDIA 檢驗證書即可向 TÜV、SGS 等機構取得最終認證，大幅降低時間與成本。生態系涵蓋 43 家以上公司（Agility、Boston Dynamics、Infineon、NXP 等），並開放 Halos Core 早期存取與 GitHub Outside-In Blueprint，支援 warehouse-deploy 與 halos-deploy Agent Skills 快速部署。

## 結論
NVIDIA Halos for Robotics 解決了非結構化環境中機器人安全的核心挑戰——將自動駕駛領域的驗證安全基礎完整移植至物理 AI 領域，從硬體安全島、認證作業系統、Outside-In 安全藍圖到第三方檢驗 Lab，構成完整的端到端安全生態系，推動產業從臨時安全實作邁向共享、標準化的安全基礎，讓機器人在複雜環境中能安全地維持全速運作。

---
