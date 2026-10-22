# Hardware-backed security at global scale: Confidential G4 with NVIDIA Blackwell is GA

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-22
- **原文連結**: https://cloud.google.com/blog/topics/ai-infrastructure/confidential-g4-gpus-are-ga/

## 核心主題
Google Cloud 正式推出基於 NVIDIA Blackwell GPU 的保密 G4 虛擬機器，提供硬件級別的數據保護，同時保持高性能。

## 關鍵重點
- **全球推出**：Confidential G4 虛擬機器現在已在全球 36 個區域正式推出，支援 Compute Engine VM 和 GKE 節點
- **端到端保密**：使用硬件強制執行執行環境來加密數據和模型參數，保護知識產權和客戶輸入免受主機系統管理員、虛擬化層和雲端提供商的訪問
- **性能優異**：測試顯示與標準 G4 相比，吞吐量下降小於 3.5%，延遲增加約 5.2%，對於 AI 推理工作負載而言性能相當
- **無需代碼重構**：使用標準 Ubuntu OS 圖像、NVIDIA 驅動器和 NVIDIA CUDA-X 庫即可部署模型，無需應用更改或自訂構建
- **多方數據合作**：即將推出一般可用性的 Confidential Space，可安全運行協同分析器和聯合模型訓練，多方可結合敏感數據而無需向彼此揭示底層私有數據

## 結論
Confidential G4 為企業提供了在雲端部署高價值模型並保護關鍵數據資產的解決方案，同時保持性能、靈活性和操作簡單性。通過提供可驗證的信任能力和強大的硬件隔離，組織可以在雲規模上安全地部署高價值模型並保護關鍵數據資產。

---