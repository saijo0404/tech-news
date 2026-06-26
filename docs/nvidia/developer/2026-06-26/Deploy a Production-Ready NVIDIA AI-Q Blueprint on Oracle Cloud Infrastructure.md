---
# Deploy a Production-Ready NVIDIA AI-Q Blueprint on Oracle Cloud Infrastructure

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-26
- **原文連結**: https://developer.nvidia.com/blog/deploy-a-production-ready-nvidia-ai-q-blueprint-on-oracle-cloud-infrastructure/

## 核心主題
NVIDIA 與 Oracle 合作發布部署指南，示範如何透過 Terraform 與 Helm 在 Oracle Cloud Infrastructure（OCI）上一鍵部署 AI-Q 2.0 多智能體系統，讓開發者能快速在雲端建立生產級 AI Agent 端點。

## 關鍵重點
- **AI-Q 多智能體架構**：AI-Q 2.0 基於 LangChain Deep Agents 與 NeMo Agent Toolkit 建置，採用意圖路由器（Intent Router）將使用者查詢分發至淺層研究智能體（快速搜尋）或深度智能體（含規劃與研究子智能體），支援沙箱環境中的工具執行與長程任務規劃。
- **OCI 基礎設施自動化部署**：使用 Terraform 模組自動建立 VCN、OKE Kubernetes 集群、負載平衡器與 OCI Vault 金鑰管理；再以 Helm Chart 安裝三個工作負載——後端 FastAPI 伺服器、前端 Next.js Web UI，以及叢集內 PostgreSQL 資料庫。整體部署約需 20–25 分鐘，並以單一 `terraform destroy` 命令即可完整移除。
- **完整操作步驟與疑難排解**：指南涵蓋從設定 Terraform 變數、建立基礎設施、配置 kubectl 連線、建立 API 金鑰 Secret、拉取並安裝 Helm Chart 到最後開啟 Web 介面的完整流程，並提供 ImagePullBackOff、PVC 未動態配置、LB IP 為 null 等常見問題的排除方法。

## 結論
此部署藍圖將 NVIDIA 最先進的多智能體 AI 架構與 OCI 雲端基礎設施緊密整合，透過 IaC（基礎設施即程式碼）與 Kubernetes 自動化，大幅降低企業部署 AI Agent 的門檻。所有組件均可透過 YAML 配置與 NeMo 插件系統進行擴充，實現模型替換、子智能體新增與 RAG 後端串接，為雲端 AI 應用開發提供了即開即用的生產級解決方案。

---
