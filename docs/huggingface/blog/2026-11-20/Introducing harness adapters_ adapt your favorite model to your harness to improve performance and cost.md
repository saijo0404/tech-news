# Introducing harness adapters - adapt your favorite model to your harness to improve performance and cost

- **來源**: Hugging Face Blog
- **發布日期**: 2026-11-20
- **原文連結**: https://huggingface.co/blog/harness-adapters-at-scale

## 核心主題
Hugging Face 團隊開發了 harness adapters 技術，通過在目標 harness 內部進行 RL 訓練，使特定模型（如 Qwen3.8-27B）能更精確、高效地適應特定任務環境，同時提升性能並降低成本。

## 關鍵重點
- 訓練了三個專精適配器分別針對 Pi、OpenCode 和 Hermes Agent harness，在各自環境上表現優於基礎模型
- 使用 RL 訓練方法（AsyncGRPOTrainer）在 harness 內部進行訓練，數據集包含 750 個 RL 環境任務 + 300 個 Termgrade 任務
- 性能提升顯著：Terminal-Bench 2.1 從 39% 提升至 55%，SWE-bench Pro 提升 6-20 分，工具調用減少 53-73%，token 減少 44-60%
- 可跨 harness 通用：訓練後的 adapter 可合併成單一 super adapter，所有 artifacts 可在 Hugging Face 上瀏覽和重現
- 安全機制：使用 safeagents 工具阻止不當行為，訓練期間成功阻擋 647 次工具調用
- 訓練過程可重複應用於其他模型，具有可移植性

## 結論
Hugging Face 團隊通過 harness adapters 技術成功實現了模型在特定任務環境中的精確適應，顯著提升了性能並降低了成本，同時保持了訓練過程的可重複性和可移植性。
---