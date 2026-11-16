# Introducing AlphaProof Code: a breakthrough in verifying complex software at depth

- **來源**: Google DeepMind
- **發布日期**: 2026-11-10
- **原文連結**: https://deepmind.google/blog/introducing-alphaproof-code/

## 核心主題
Google DeepMind 開發了 AlphaProof Code，首次使用 AI 代理框架對 Signal 加密協議的實際程式碼進行了形式化驗證，解決了長期被視為重大安全挑戰的複雜軟體驗證問題。

## 關鍵重點
- **AI 代理框架**：AlphaProof Code 是一個多 LLM 代理框架，將形式驗證工作分成兩部分：人類專家與 AI 合作決定證明什麼，AI 代理（Gemini Carbon）則執行證明工作。
- **大規模驗證成果**：AI 代理生成了超過 600 萬行 Lean 程式碼，用於數學證明 Signal 協議的安全性，並自動檢查證明結果。
- **突破性成就**：這是首次 AI 用於形式驗證廣泛部署的加密協議，也是首次任何方法（含或不含 AI）對廣泛部署協議的實現進行形式化驗證。
- **效率提升**：驗證過程只花了四週，而傳統上專家團隊需要數年才能完成的工作。
- **完整驗證範圍**：驗證涵蓋了從設計到實際編譯代碼的完整鏈，確保設備上的代碼符合安全屬性，填補了設計與實現之間的漏洞。

## 結論
這項突破展示了 AI 如何將精英級別的安全保證帶到企業、政府和關鍵基礎設施中，並為驗證其他重要系統（如醫療設備固件和電力網軟體）奠定基礎。Google DeepMind 已開放源碼其形式驗證 artifacts，供社群使用。

---

此摘要已儲存至指定檔案路徑。