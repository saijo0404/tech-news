# Introducing Kinference: An Open Source Inference Control Plane for vLLM and Kubernetes

- **來源**: vLLM Blog
- **發布日期**: 2026-11-04
- **原文連結**: https://vllm.ai/blog/2026-11-04-introducing-kinference

## 核心主題
Kinference 是由 Buoyant 開發的開源項目，旨在構建基於 vLLM 的可擴展推理平台，提供完整的推理控制平面功能。

## 關鍵重點
- **KV 快取感知的負載平衡**：Kinference 能根據 GPU 快取內容、歷史性能和 GPU 佇列大小進行智能負載分配，相比標準 Kubernetes 負載平衡，TTFT 降低 95%，延遲降低 45%。
- **政策驅動的方法**：透過 YAML 政策允許平台所有者根據使用者、模型類型、GPU 狀態和請求複雜度等條件，靈活決定推理請求的路由策略。
- **全面的指標與 SLOs**：提供完整的推理相關指標，包括 token 速率、TTFT/ITL/E2E 延遲分佈、快取狀態、模型使用率和 GPU 飽和度等，支持按租户追蹤。
- **易於整合**：只需將推理客戶指向 Kinference 的 HTTP 端點即可使用，可與現有 Kubernetes 堆疊搭配。

## 結論
Kinference 為開發者提供了完整的推理平台控制平面解決方案，透過政策驅動的路由和 KV 快取感知的負載平衡，顯著提升了推理平台的性能和靈活性，是構建現代化推理平台的理想選擇。
---
