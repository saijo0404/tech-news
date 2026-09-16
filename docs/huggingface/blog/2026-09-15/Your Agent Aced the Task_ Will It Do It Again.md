# Your Agent Aced the Task. Will It Do It Again?

- **來源**: Hugging Face Blog
- **發布日期**: 2026-09-15
- **原文連結**: https://huggingface.co/blog/ibm-research/altk-evolve-consistency

## 核心主題
IBM Research 團隊介紹了 ALTK-Evolve 系統中的「一致性指南（consistency guidelines）」，用於解決 AI 代理在相同任務上表現不一致的可靠性問題。

## 關鍵重點
- **一致性差距（Consistency Gap）**：Mean@k（平均成功率）與 Pass^k（所有嘗試都成功的比例）之間的差距，揭示了 AI 代理的可靠性問題。例如 GPT-4.1 在 AppWorld 測試中，平均成功率 77.4%，但所有嘗試都成功的比例僅 53.0%，差距達 24.4%。
- **一致性分析器（Consistency Analyzer）**：一種診斷工具，通過重採樣代理的決策軌跡，找出容易出錯的決策點（flip-prone decision points），無需重新執行任務即可識別不穩定決策。
- **一致性指南（Consistency Guidelines）**：基於分析結果生成的指導規則，將一致性差距從 24.4% 降低到 12.0%，同時不影響平均準確率。例如在計數任務中，通過使用行錨定正則表達式替代簡單子串計數，提高了結果一致性。
- **一般化能力**：生成的指南不僅適用於相同任務，還能在相關任務上提升 13.0% 的 Pass^5，證明其具有跨任務的泛化能力。

## 結論
AI 代理的準確性無法完全反映其可靠性。通過引入一致性分析器和一致性指南，可以顯著降低一致性差距，使 AI 代理在關鍵任務中更具可信度。這為部署 AI 代理提供了更可靠的評估和改進方式，特別適合金融交易對接、合約審查等關鍵任務場景。

---

完整技術報告可參考：https://arxiv.org/abs/2609.08832