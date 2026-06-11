---
# The Open Source Community is backing OpenEnv for Agentic RL

- **來源**: Hugging Face Blog
- **發布日期**: 2026-06-08
- **原文連結**: https://huggingface.co/blog/openenv-agentic-rl

## 核心主題
OpenEnv 宣布由 Meta-PyTorch、Reflection、Unsloth、Modal、Nvidia 與 Hugging Face 等機構組成委員會共同治理，並遷移至 Hugging Face，致力於打造開源代理強化學習的共通基礎設施。

## 關鍵重點
- **為什麼需要 OpenEnv**：閉環系統如 Claude Code 與 Codex 能透過模型與 harness 深度優化獲得強大效能，但開源生態需要模型、harness 與推論引擎自由組合的彈性；OpenEnv 作為環境、harness 與訓練器之間的介面層，讓任何模型都能驅動任何環境而無需客製程式。
- **協議層而非獎勵框架**：OpenEnv 明確定位為互操作性層，標準化環境如何發布、部署與被代理消費；它使用 Gymnasium 風格 API（reset、step、state）與 HTTP/WebSocket 協定、Docker 包裝，並將 MCP 列為一等公民，讓環境在模擬與生產模式下行為一致，但不干預獎勵定義或訓練迴圈。
- **下一步重點**：透過 Hugging Face Datasets 串接任務集（RFC 006）、允許外部獎勵庫獨立定義獎勵（RFC 007）、持續整合各類代理 harness、提供 TRL 與 Unsloth 的端到端教學，以及開發自動環境驗證機制（RFC 008）以衡量環境品質與對模型學習的貢獻。

## 結論
OpenEnv 由社群設計並由多組織共同治理，旨在成為開源代理 RL 的通用底層；雖然目前仍在早期階段、可能存在不完美之處，但已有超過二十個領先組織支持，社群正邀請更多人參與共同塑造這個基礎設施的未來。

---
