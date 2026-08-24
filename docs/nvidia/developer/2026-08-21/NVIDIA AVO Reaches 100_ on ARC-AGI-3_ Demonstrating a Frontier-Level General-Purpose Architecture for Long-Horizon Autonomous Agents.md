# NVIDIA AVO Reaches 100% on ARC-AGI-3, Demonstrating a Frontier-Level General-Purpose Architecture for Long-Horizon Autonomous Agents

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-08-21
- **原文連結**: https://developer.nvidia.com/blog/nvidia-avo-reaches-100-on-arc-agi-3-demonstrating-a-frontier-level-general-purpose-architecture-for-long-horizon-autonomous-agents/

## 核心主題
NVIDIA 的 AVO（Agentic Variation Operators）架構在 ARC-AGI-3  benchmarks 上達到 100% 表現，證明系統架構設計比單一模型能力更重要，可實現長期自主任務的前鋒級性能。

## 關鍵重點
- **GPU 核心優化突破**：AVO 自主探索超過 500 個優化方向，提交 40 個核心版本，在 NVIDIA DGX B200 系統上比 FlashAttention-4 快 10.5%，展現無人工介入的生產力工程循環。
- **ARC-AGI-3 完美表現**：使用 Claude Opus 5 在 25 個環境中完成所有 183 個等級，獲得 100.00 RHAE 分數，比 VISTA 系統少用 12% 的環境動作。
- **系統架構勝過模型能力**：模型能力至關重要，但周圍的代理系統（harness）決定如何有效將能力轉化為持續自主進步，系統層面的架構設計比單一模型能力更重要。
- **持久化記憶與監督機制**：AVO 透過持久化記憶保存先前實現、評估結果和推理，透過監督機制監控進度和重定向策略，使代理能在長期任務中持續進步。
- **跨領域架構可移植性**：AVO 架構從 GPU 核心優化成功轉移至 ARC-AGI-3 互動推理任務，證明其通用性不侷限於軟體工程，而是掌握長期自主進步的機械。

## 結論
AVO 架構的成功證明，要實現長期自主任務的前鋒級性能，關鍵不在於使用更強大的模型，而在於設計能夠持續累積證據、維持進度、從錯誤中恢復的完整系統架構。這為未來通用代理系統的發展提供了重要指引。

---