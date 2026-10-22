# How NVIDIA OpenShell Reference Architecture Secures and Governs AI Agent Workloads at Scale

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-10-21
- **原文連結**: https://developer.nvidia.com/blog/how-nvidia-openshell-reference-architecture-secures-and-governs-ai-agent-workloads-at-scale/

## 核心主題
這篇文章介紹了 NVIDIA OpenShell 參考架構，這是一個開源運行時環境，用於確保和治理大規模 AI 代理工作負載，通過將代理工作負載視為不可信並僅在需要時授予訪問權限。

## 關鍵重點
- OpenShell 使用四個組件（Gateway、Supervisor、Sandbox 和 Policy Prover）來管理沙盒生命週期、中介憑證訪問、隔離工作負載並正式驗證政策許可權。
- NVIDIA Vera CPU 具有 88 個 Olympus 核心、第二代可擴展一致性布線和 LPDDR5X 記憶體，相比 x86 在關鍵代理任務上提供高達 2 倍的效能。
- CoreWeave 測試顯示，在 Vera 上沙盒啟動速度快 3 倍以上，代理循環完成速度快 1.8 倍，單一機架可支援超過 11,000 個並行代理環境。
- NVIDIA BlueField-4 DPU 和 NVIDIA Sentry 提供硬體隔離的監控和在矽中強制執行，可在毫秒內隔離違規的代理。

## 結論
OpenShell 參考架構與 NVIDIA Vera CPU 和 BlueField-4 DPU 共同構成了安全 AI 代理的完整堆疊，為組織提供性能以使代理高效運作，同時通過外部強制執行的策略保持工作範圍在授權邊界內。
---
