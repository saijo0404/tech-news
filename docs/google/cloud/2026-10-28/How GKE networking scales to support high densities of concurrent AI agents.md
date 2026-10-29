# How GKE networking scales to support high densities of concurrent AI agents

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-29
- **原文連結**: https://cloud.google.com/blog/products/networking/gke-networking-dataplane-for-large-agentic-ai-workloads/

## 核心主題
這篇文章介紹了 GKE Dataplane V2 如何通過優化網路身份管理、解決身份擴展限制，實現次秒級 provisioning，以支持高密度的 AI 代理工作負載。

## 關鍵重點
- GKE Dataplane V2 使用 eBPF 技術將 Pod 標籤映射為數值身份，解決了傳統方法中每個 Pod 都需要獨特標籤所帶來的擴展限制問題。
- 通過將高基数數據從標籤移至註釋，並應用 Cilium 標籤過濾規則，GKE 可以避免 65,536 個網路身份的集群限制。
- Agent Sandbox 和 Agent Substrate 提供了安全、輕量級的隔離，支持每秒 300 個沙盒的超低延遲啟動，並可擴展至每秒 500 次激活。

## 結論
GKE Dataplane V2 通過優化網路身份計算和過濾高基数元數據，解決了大型 AI 工作負載中的關鍵基礎設施瓶頸，降低了沙盒 provision 延遲，減少了昂貴的 GPU 閒置時間，並有助於維持高計算密度。
---