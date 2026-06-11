---
# One-Click Multi-Tenant Security with NVIDIA Quantum InfiniBand

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-11
- **原文連結**: https://developer.nvidia.com/blog/one-click-multi-tenant-security-with-nvidia-quantum-infiniband/

## 核心主題
NVIDIA Quantum InfiniBand 在 Unified Fabric Manager（UFM）中推出基於意圖的安全配置文件（intent-based security profiles），讓雲端提供商能一鍵部署多租戶網絡安全，將部署時間從數小時或數天縮短至數分鐘，支援數萬張 GPU 的硬體級租戶隔離。

## 關鍵重點
- **三種安全配置文件**：（1）General——單一租戶環境的預設配置；（2）Bare Metal Cloud——針對多租戶雲端環境，以 PKey 隔離實現租戶分離，類似 Ethernet VLAN 但以硬體機制防止分區間越權存取；（3）Secured Bare Metal Cloud——針對高安全需求的多租戶環境，在 PKey 基礎上增加 MAD 金鑰保護、GUID 存取控制、服務級認證、MAD 速率限制、DoS/DDoS 防護與基於來源的速率限制等全方位安全措施。
- **意圖配置的核心優勢**：相較於傳統網路端點各自決策導致配置錯誤與不一致，UFM 集中控制確保全局策略一致性；意圖配置文件實現更少錯誤（以 NVIDIA 工程預期方式部署安全功能）、配置時間縮減（從數小時至數分鐘）、零觸控擴展（增加節點不需線性增加管理開銷），以及無安全 downtime（新功能直接加入配置文件無需過渡期）。
- **持續安全驗證（CSV）與健康檢查**：UFM 新增 Continuous Security Verification（CSV）診斷功能，透過靜態分析與日誌審計生成「安全健康分數」，並提供自動化的漏洞修復步驟；使用者可在 UFM Cyber AI 的 System Health Security 儀表板選擇不同詳細程度（錯誤、錯誤與警告、資訊）產生安全驗證報告，確保網絡安全態勢可持續監控。

## 結論
NVIDIA 以意圖配置文件將 InfiniBand 進階安全能力民主化，彌補了企業從傳統以太網遷移至 InfiniBand 時的領域知識缺口，讓雲端提供商能在千級交換器與萬級 GPU 規模下，以單一點擊實現硬體強制執行、加密與邏輯分離的多租戶安全架構。

---
