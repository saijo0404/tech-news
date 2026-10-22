# How Specializing the Vocabulary of SLMs Can Cut Inference Cost by 77% in Real Applications

- **來源**: Hugging Face
- **發布日期**: 2026-10-21
- **原文連結**: https://huggingface.co/blog/Dharma-AI/vocabx-vocabulary-specialization

## 核心主題
Dharma-AI 開發的 VocabX 方法通過將詞彙專門化（而非按頻率），在保持基礎模型不變的情況下，將推理成本降低了 77%。

## 關鍵重點
- 傳統 tokenizer 對單一領域模型造成碎片化（將重複序列拆成多個 token）和浪費（包含領域從未使用的詞彙）
- 生成 token 的成本是讀取 token 的 7.4 倍（因為 decode 階段是記憶體頻寬受限）
- VocabX 同時優化兩個層級：子詞層（sub-word）和多詞層（multi-word/macros），並基於成本而非頻率選擇 token
- 在葡萄牙語作文評分器上測試，從 151,669 個詞彙表項減少到 64,767 個，推理成本降低 77%

## 結論
VocabX 證明通過詞彙專門化可以大幅降低推理成本，同時保持模型品質。這表明在特定領域應用中，重新設計 tokenizer 比單純優化模型參數更能帶來顯著效益。
---
