# Thinking of ACE? We Can Do It with Fewer Tokens

- **來源**: Hugging Face Blog
- **發布日期**: 2026-08-11
- **原文連結**: https://huggingface.co/blog/ibm-research/altk-evolve-sldd

## 核心主題
IBM Research 團隊比較了兩種智能體記憶系統 ACE 與 ALTK-Evolve，發現通過更智能的記憶交付方式，可以在保持或提升準確性的同時大幅降低推理成本。

## 關鍵重點
- ACE 與 ALTK-Evolve 都讓智能體從自身歷史軌跡學習，但 ACE 總是發送完整的 playbook，而 ALTK-Evolve 根據模型能力動態選取 guidelines
- 在 DeepSeek-V3.2 上，ALTK-Evolve 比 ACE 少用約 40% 的 token；在 gpt-oss-120b 上，ALTK-Evolve 僅用 ACE 約 1/7 的 token
- 準確性方面：DeepSeek-V3.2 上 ALTK-Evolve 整體表現更好，gpt-oss-120b 上兩者表現相當（ALTK-Evolve 略優）
- 核心差異在於交付策略：ALTK-Evolve 採用按需選取而非固定發送，避免對弱模型造成干擾

## 結論
ALTK-Evolve 通過動態調整記憶交付量，在保持或提升準確性的同時實現顯著的成本優化，特別適合資源受限的模型場景。
---
