# Add Runtime Controls to AI Agents with NVIDIA OpenShell

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-09-28
- **原文連結**: https://developer.nvidia.com/blog/add-runtime-controls-to-ai-agents-with-nvidia-openshell/

## 核心主題
NVIDIA OpenShell 0.1.0 是一個開源運行時環境，可在不修改 AI 代理的情況下，強制執行其可訪問的系統和數據範圍。

## 關鍵重點
- OpenShell 結合了沙盒執行、受控服務訪問、憑證管理和正式政策分析，以限制 API 操作並保護代理工作負載之外的憑證。
- 包括 Cadence、Slack 和 Gecko Robotics 在內的組織正在採用 OpenShell，用於芯片設計、企業自動化以及物理機器人治理。
- OpenShell 提供三個組件（Gateway、Supervisor 和 Sandbox）來管理代理fleet，檢查出站請求是否符合政策，並應用内核級的文件系統和進程控制。
- 政策證明器使用形式邏輯來驗證建模的權限是否保持在定義的邊界內，並識別超出邊界的動作。
- 團隊可以本地使用沙盒進行開發，並使用工作空間、Docker 和 Kubernetes 的計算驅動程序以及可信中間件將代理部署到共享基礎設施中。

## 結論
NVIDIA OpenShell 為現有 AI 代理提供了可強制執行的運行時控制，使團隊能夠限制 API 操作、保護憑證並審查權限變更，而不需要重写代理。

---