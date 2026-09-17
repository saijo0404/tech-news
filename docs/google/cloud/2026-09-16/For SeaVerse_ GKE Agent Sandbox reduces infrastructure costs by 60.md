# For SeaVerse, GKE Agent Sandbox reduces infrastructure costs by 60%

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-17
- **原文連結**: https://cloud.google.com/blog/products/containers-kubernetes/seaverse-chooses-gke-agent-sandbox/

## 核心主題
SeaVerse 使用 Google Cloud 的 GKE Agent Sandbox 技術，成功將基礎設施成本降低 60%，同時提供強大的多租戶隔離能力和可觀測性，支持可玩 AI 體驗的快速開發。

## 關鍵重點
- **成本降低 60%**：透過 GKE Agent Sandbox 的靈活性，可以根據工作負載大小精確分配資源，大幅降低基礎設施成本。
- **強大的隔離與可觀測性**：提供 kernel-level 隔離（支援 Kata Containers+Cloudhypervisor 和 gVisor），同時具備原生可觀測性，讓開發者能更快診斷問題。
- **高效能的資源分配**：支援每秒最多 300 個沙盒分配，90% 的分配可在 200 毫秒內完成，確保使用者體驗的即時性。
- **支援多租戶環境**：提供清晰的用戶、創作和沙盒之間的安全邊界，同時保持快速創作循環。
- **持久化儲存支援**：現在可以為工作負載附加持久化儲存，支援更複雜的使用案例。

## 結論
透過採用 GKE 和 GKE Agent Sandbox，SeaVerse 不僅大幅降低了基礎設施成本，還建立了更穩定、可擴展且易於管理的 AI 基礎設施，為下一代可玩 AI 體驗奠定了更堅實的基礎。
---