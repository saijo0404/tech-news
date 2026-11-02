# Build Specialized Agents on a Stack You Control with NVIDIA NemoClaw

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-10-30
- **原文連結**: https://developer.nvidia.com/blog/build-specialized-agents-on-a-stack-you-control-with-nvidia-nemoclaw/

## 核心主題
這篇文章介紹了 NVIDIA NemoClaw 如何幫助開發者建立專用的 AI 代理，提供開源藍圖，整合調優的代理框架、Nemotron 模型、NeMo 優化工具和 OpenShell 安全運行時。

## 關鍵重點
- NemoClaw 提供開源藍圖，支援 OpenClaw、Hermes Agent 和 LangChain Deep Agents 三種代理框架，讓開發者可以保留現有框架並添加模型優化、可觀測性和治理功能。
- LangChain 將其 Deep Agents 框架針對 Nemotron 3 Ultra 進行了調優，實現了接近前沿的性能，每運行成本降低約 10 倍。
- OpenShell 作為安全運行時，管理代理對檔案、網路、憑證和工具的訪問，確保即使記憶或檢索上下文暗示不當行為，代理仍受政策約束。
- NemoClaw 代理可在雲端、數據中心、NVIDIA DGX Spark 和 NVIDIA RTX PC/工作站上運行，並可與 Claude、Codex 或 Cursor 等前沿代理協同工作。

## 結論
NemoClaw 為開發者提供了在自定義堆疊上建立專用代理的完整解決方案，結合了模型與框架的協同優化、可觀測性和安全治理，使代理既能高效運行又能安全操作。

---