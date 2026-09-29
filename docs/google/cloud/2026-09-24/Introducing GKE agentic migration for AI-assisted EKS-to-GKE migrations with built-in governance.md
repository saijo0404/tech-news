# Introducing GKE agentic migration for AI-assisted EKS-to-GKE migrations with built-in governance

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-25
- **原文連結**: https://cloud.google.com/blog/products/containers-kubernetes/gke-agentic-migration/

## 核心主題
Google 推出 GKE agentic migration，這是一個開源代理插件，用於將 AWS EKS 環境遷移至 GKE，結合 AI 能力與確定性防護機制。

## 關鍵重點
- **混合驗證機制**：LLM 生成內容經過確定性驗證，避免幻覺風險。LLM 負責複雜的 Terraform 和 Kubernetes YAML 編寫，伺服器則執行確定性轉換以確保映射準確。
- **GitOps 原生 PR 工作流**：所有變更通過 Pull Request 流程，避免直接修改生產集群（ClickOps），確保所有變更都經過標準的 HITL CI/CD 審查流程。
- **保護的翻譯與傳輸分離**：自動化架構翻譯邏輯，但有意避免傳輸狀態數據，以保護敏感資產。插件會生成情境化操作手冊，指導團隊使用 Google Cloud 專用的 SLA 支援工具（如資料庫遷移服務或儲存轉移服務）。
- **多人格狀態管理**：支持平台工程師與應用開發者之間的保護性協作。插件會持久化長期遷移狀態，允許團隊成員在權限隔離的資料夾中獨立工作。

## 結論
GKE agentic migration 將雲遷移從分散的重新編寫練習轉化為可預測、AI 輔助且可審查的 GitOps 工作流，大幅降低執行風險與不可預測性。

---