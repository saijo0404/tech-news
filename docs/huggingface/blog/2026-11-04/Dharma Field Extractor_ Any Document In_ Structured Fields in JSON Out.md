# Dharma Field Extractor: Any Document In, Structured Fields in JSON Out

- **來源**: Hugging Face
- **發布日期**: 2026-11-04
- **原文連結**: https://huggingface.co/blog/Dharma-AI/dharma-field-extractor

## 核心主題
Dharma-AI 推出了一個20億參數的模型，能從任何文件類型中提取特定字段，並輸出結構化的 JSON 格式，性能優於所有前沿 LLM，且成本更低。

## 關鍵重點
- 提供兩種模式：Open 模式（無 schema，模型自動識別字段）和 Schema-directed 模式（指定 exact schema，模型按指定格式輸出）
- 在 benchmark 測試中，性能得分 0.834，優於 Claude Opus 5 (0.816) 和 GPT-5.6 Luna (0.741)
- 成本優勢顯著：相比 GPT-5.6 Luna 便宜6倍，相比 GPT-5.6 Sol 便宜147倍
- 基於 DharmaOCR-LITE v1.1 基礎模型，使用 LoRA 技術在43,384個訓練示例上進行訓練
- 訓練數據涵蓋多語言和多領域：英語多領域數據、巴西語域數據和多語言數據

## 結論
這是一個證明在特定任務上，專注訓練的小模型可以超越通用前沿模型的最佳案例，同時大幅降低成本。
---