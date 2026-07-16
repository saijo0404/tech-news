# Securing the AI supply chain on GKE: Introducing k8s-aibom for automated AI BOMs

- **來源**: Google Cloud Blog
- **發布日期**: 2026-07-14
- **原文連結**: https://cloud.google.com/blog/products/identity-security/introducing-k8s-aibom-on-gke-for-automated-ai-bills-of-materials/

## 核心主題
Google 推出 k8s-aibom 開源控制器，自動監控 Kubernetes 集群並生成 AI 物料清單（BOM），解決影子 AI 問題。

## 關鍵重點
- 輕量級、無權限設計，無需開發者修改 pod 配置、無需側車容器或權限 DaemonSet
- 自動檢測 AI 運行時（如 vLLM、Triton、LangChain 等）並生成符合 OWASP CycloneDX 1.6 標準的 ML-BOM
- 基於確定性信心模型，將發現的資產分為「已聲明」、「推斷」和「未解決」三類，協助合規審計

## 結論
k8s-aibom 幫助團隊安全將 AI 項目從測試階段推進到生產環境，同時滿足 EU AI Act、NIST AI RMF 等全球合規框架要求，提供不可篡改的審計日誌。

---