# Inside NVIDIA Sentry: Secure AI Agents at Runtime

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-10-21
- **原文連結**: https://developer.nvidia.com/blog/inside-nvidia-sentry-secure-ai-agents-at-runtime/

## 核心主題
NVIDIA Sentry 是一個在 BlueField-4 DPU 上運行的硬體隔離安全框架，用於監控 AI 代理並強制執行訪問政策，確保 AI 代理在設計意圖和運營邊界內運行。

## 關鍵重點
- **DOCA Tower**：作為透明代理終止 TLS 並使用 Open Policy Agent (OPA) 評估代理請求，基於容器哈希、進程完整性等政策進行授權。
- **DOCA Argus**：提供實時記憶體內省，獨立於主機分析執行環境，追蹤容器、進程和加載庫的哈希值以驗證安全性。
- **專用 AI 模型**：對代理通訊進行線上或離線分類，檢測行為漂移並可毫秒級內存封鎖威脅。
- **硬體信任域保護**：在 BlueField-4 的硬體信任域中運行，即使主機被入侵也能保持監控和強制執行能力。
- **tamper-evident 記錄**：使用 BlueField-4 的獨立信任域保存不可篡改的遥測數據，支援企業安全平台整合。

## 結論
NVIDIA Sentry 通過硬體隔離的安全層，為 AI 代理提供獨立於軟體邊界的實時監控和強制執行能力，有效防止代理越權和行為漂移，同時提供可驗證的審計追蹤記錄。

---