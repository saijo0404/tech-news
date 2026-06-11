---
# Powering the next era of Confidential AI

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-11
- **原文連結**: https://cloud.google.com/blog/products/identity-security/powering-the-next-era-of-confidential-ai/

## 核心主題
Google Cloud 宣布與 Apple 合作，在 Google Cloud 基礎設施上部署 Apple Private Cloud Compute（PCC），以 Google 的 Confidential Computing、Titanium 安全架構及 Intel TDX、NVIDIA 安全技術，為高敏感 AI 工作負載提供硬體級別的資料加密與隔離保障。

## 關鍵重點
- **Apple PCC 擴展至 Google Cloud**：Google Cloud 與 Apple 合作打造符合 Apple 嚴苛安全、機密性與透明度目標的 PCC 服務平台，整合 Intel TDX（信任域擴展）與 NVIDIA Confidential Computing，為虛擬機器提供硬體級隔離，確保 AI 推理過程中 CPU 到 GPU 的完整計算路徑均受保護。
- **Titanium 安全架構與硬體信任根**：Google 自研 Titan 晶片部署於整個機隊，提供硬體級信任根，確保開機流程與硬體平台的完整性；Confidential Computing 則在此基礎上確保資料在靜態、傳輸中及使用時均以加密狀態運行於可信執行環境（TEEs）內，防止未授權存取。
- **開源主機堆疊與透明稽核**：Apple 與 Google 共同設計開源主機堆疊，專門支援 PCC 的透明度需求，使第三方能夠獨立檢視與驗證系統的安全屬性，實現可驗證的安全保障、無特權執行期存取與強制性防護。

## 結論
這項由 Apple、Google Cloud、Intel 與 NVIDIA 四方協作的成果標誌著私密 AI 基礎設施的重大里程碑，所建立的先進平台不僅滿足 Apple PCC 的嚴格標準，其安全技術也惠及所有 Google Cloud 客戶，為處理 AI 與敏感資料的工作負載提供更透明、更安全、更具韌性的平台。

---
