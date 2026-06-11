---
# Migrating Your GitHub CI to Hugging Face Jobs

- **來源**: Hugging Face Blog
- **發布日期**: 2026-06-09
- **原文連結**: https://huggingface.co/blog/github-ci-hf-jobs

## 核心主題
Hugging Face 團隊展示如何將 GitHub Actions 的 CI 工作負載轉移至 Hugging Face Jobs 伺服器基礎設施，透過開源的 `jobs-actions` 橋接器，實現 CPU 測試速度提升 30% 並新增 GPU 硬體測試能力。

## 關鍵重點
- **架構：GitHub App + 零時執行器**：建立一個 Dispatcher Space 接收 GitHub `workflow_job.queued` webhook，驗證後產生短壽命 GitHub 執行器註冊權杖並啟動對應硬體（如 `hf-jobs-t4-small`）的 HF Job，從 GitHub 視角看即為自託管執行器，從 HF 視角看即為執行 Workflow 步驟的容器 Job。
- **五步驟設定流程**：（1）複製 Dispatcher Space 並選擇 `cpu-upgrade` 硬體維持可用性；（2）在 Space 中建立 GitHub App 並安裝到目標倉庫；（3）上傳 App 憑證、webhook 金鑰與 HF Token 至 Space；（4）將 workflow 中的 `runs-on` 替換為 `hf-jobs-cpu-upgrade` 或 `hf-jobs-t4-small` 等標籤；（5）透過 CLI 測試驗證。
- **實際成效與注意事項**：Trackio 專案的 CPU 測試從 1 分 40 秒縮短至 1 分 10 秒（節省 30%），GPU 測試僅需 45 秒且費用低於一美分；選用適當 Docker 映像（如 Playwright 官方映像）可避免每次重複安裝系統套件，HF Jobs 的 CLI 日誌取得也方便本地檢查與 agent 除錯。

## 結論
Hugging Face Jobs 提供了一個低成本、高彈性的 GitHub CI 後端方案，特別適合需要自訂 Docker 映像、GPU 硬體或更快測試週期的機器學習專案；設定流程已全面支援 CLI 與 agent 協助，讓開發者能輕鬆將 CI 遷移並獲得實質效能提升。

---
