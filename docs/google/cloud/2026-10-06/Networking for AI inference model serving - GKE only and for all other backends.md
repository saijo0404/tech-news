# Networking for AI inference model serving - GKE only and for all other backends

- **來源**: Google Cloud Blog Developers & Practitioners
- **發布日期**: 2026-10-07
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/networking-for-ai-inference-model-serving-gke-only-and-for-all-other-backends/

## 核心主題
這篇文章介紹了兩種 AI 推理模型服務網路架構參考設計，分別是針對 GKE 單一後端和多種後端類型（如 Cloud Run、Agent Platform 等）的架構。

## 關鍵重點
- **共同服務架構**：兩種設計都包含 Private Service Connect inference endpoint（將流量限制在私有 VPC 網路）、可選的 Apigee API Management（用於身份驗證、速率限制和配額管理），以及 Model Armor（作為 AI 安全檢查點，篩檢提示和輸出以預防提示注入和敏感資料洩漏）。
- **GKE 專屬架構**：使用 GKE Inference Gateway 作為專用進站引擎，解析請求載體、評估 HTTPRoute 規則，並根據模型識別碼將請求路由到適當的推理池。支援推理池自動擴展和基於 Prometheus 實時資料的負載平衡。
- **多後端架構**：使用 Regional internal Application Load Balancer 作為中央 Layer 7 路由代理，搭配 Inference Payload Processor（Cloud Run 服務擴展呼叫）提取模型識別碼，透過 Network Endpoint Group (NEG) 將請求路由到異質後端（如 Agent Platform、GKE、Cloud Run、混合環境或外部雲端）。

## 結論
透過這些參考架構，開發者可以建立集中化治理、安全且可靠的 AI 推理模型服務架構，支援多種後端環境，並確保提示安全、負載平衡和私有網路傳輸。
---

檔案已成功儲存。