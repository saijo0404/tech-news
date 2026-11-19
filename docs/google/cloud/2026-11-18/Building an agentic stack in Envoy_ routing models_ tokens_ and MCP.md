# Building an agentic stack in Envoy: routing models, tokens, and MCP

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-19
- **原文連結**: https://cloud.google.com/blog/products/networking/the-envoy-agentic-stack-routing-models-tokens-and-mcp/

## 核心主題
本文介紹了 Envoy 代理如何演進以支援自主 AI 代理，透過路由模型、Token 管理和 MCP 工具呼叫來解決傳統 L7 代理的挑戰。

## 關鍵重點
- 自主代理挑戰傳統 L7 代理的四大問題：載體盲視、請求速率限制假設、無狀態負載平衡和不受管制的工具執行
- Envoy 提供四大核心支柱：原生載體解析器、Tokenomics 引擎、模型與 MCP 路由、AI 安全防護欄
- 支援 MCP 工具路由使用 JSON-RPC 2.0 和 Mcp-Method/Mcp-Name 標頭進行零載體解析路由
- 提供高密度基礎設施支援，包括零規模流量導向和出站邊境防禦

## 結論
Envoy 已演進為專為多代理架構設計的智能可擴展網路層，開發者可透過 GitHub 檢視程式碼並參與 CNCF、Gateway API 和 Kubernetes AI Gateway 工作小組。
---