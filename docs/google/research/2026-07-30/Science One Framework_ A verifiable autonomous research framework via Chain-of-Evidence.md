# Science One Framework: A verifiable autonomous research framework via Chain-of-Evidence

- **來源**: Google Research Blog
- **發布日期**: 2026-07-30
- **原文連結**: https://research.google/blog/science-one-framework-a-verifiable-autonomous-research-framework-via-chain-of-evidence/

## 核心主題
Google 推出 Science One Framework，透過 Chain-of-Evidence（鏈式證據）架構，從根本上解決 AI 自主研究中的幻覺問題，確保研究結果可驗證。

## 關鍵重點
- **現有 AI 研究系統的致命缺陷**：目前許多自主研究系統會產生不存在的引用、方法描述與代碼不一致、實驗分數無法重現等問題，幻覺率最高達 21%。
- **Chain-of-Evidence 框架的核心原則**：每個研究聲明都必須附有完整的證據鏈，且證據必須真正支持該聲明，確保可驗證性。
- **Science One Framework 的三大模塊**：問題調查者（透過 Semantic Scholar API 獲取文獻）、發現引擎（平行探索與評估解決方案）、論文撰寫與驗證器（確保所有聲明與證據一致）。
- **CoE Audit 自動化評估協議**：對 AI 生成論文進行四項完整性檢查，包括分數驗證、規範違反檢查、引用驗證和方法代碼對齊。
- **實驗結果**：Science One Framework 在可驗證性上全面領先基線系統，同時在 MLE-Bench 和 Parameter-Golf 等基準上達到最優性能，證明嚴格的可驗證性不會犧牲研究能力。

## 結論
可驗證性必須被視為第一等架構約束。Science One Framework 證明，AI 代理可以在保證研究結果可信的前提下，產生嚴謹且高度競爭的科學研究，為下一代 AI 科學家提供寶貴的驗證工具。

---