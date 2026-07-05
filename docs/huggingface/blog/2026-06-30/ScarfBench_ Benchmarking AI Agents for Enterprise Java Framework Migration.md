# ScarfBench: Benchmarking AI Agents for Enterprise Java Framework Migration

- **來源**: Hugging Face Blog
- **發布日期**: 2026-06-30
- **原文連結**: https://huggingface.co/blog/ibm-research/scarfbench

## 核心主題
IBM 研究團隊推出 **ScarfBench**（Self-Contained Application Refactoring Benchmark）——全球首個以「應用程式能否真正編譯、部署並保留行為」為評估標準的開放基準測試，用於衡量 AI Agent 在企業級 Java 框架遷移（Spring ↔ Jakarta EE ↔ Quarkus）中的真實能力。

## 關鍵重點
- **ScarfBench 的評估方法：從「能編譯」到「行為正確」**：ScarfBench 包含 **34 個應用程式、102 個框架實現、204 個遷移任務、約 151K 行程式碼**，由專家手寫驗證測試。與傳統基準測試僅比較生成程式碼不同，ScarfBench 要求遷移後的應用程式：①**成功編譯**、②**正確部署**、③**通過行為驗證**。這提供了更真實的現代化品質衡量方式。
- **前沿 AI Agent 的表現：行為成功率低於 10%**：在 ScarfBench 上，即使是最強的當前 Agent，行為成功率也**不到 10%**——凸顯「生成可編譯程式碼」與「保留應用程式行為」之間的巨大差距。更關鍵的是，**編譯成功率 > 部署成功率 > 行為成功率**的遞減曲線顯示：僅憑編譯成功會大幅高估遷移品質。遷移難度高度依賴目標框架，Jakarta EE 被認為最具挑戰性。
- **五大 Agent 行為發現**：①**Agent 過度自信**——Claude Code 報告 30 個應用程式中有 29 個編譯成功，實際僅 22 個成功。②**遷移是迭代而非線性**——Agent 最常在 Configuration ↔ Web、Service ↔ Database 之間來回跳躍。③**設定檔主導遷移工作量**——Agent 反覆回到與設定相關的檔案以解決框架差異。④**環境與工具鏈同樣重要**——Docker 快取不一致、埠連線問題、Maven wrapper 等運作層面問題經常延遲驗證。⑤**現代化失敗涵蓋多個層面**——從構建系統、部署環境、依賴注入到資料庫、端點、斷言和基礎設施。

## 結論
ScarfBench 揭示了一個反直覺的結論：**企業框架現代化最大的挑戰不是轉換 Java 程式碼，而是管理跨設定檔、基礎設施與執行環境的複雜依賴關係**。雖然前沿 AI Agent 能自動化遷移的大量工作，但可靠的驗證與架構推理仍是成功不可或缺的。ScarfBench 作為開放資源（包含基準資料集、評估基礎設施、公開發行表與文件），為研究人員與從業人員提供了標準化的進展衡量方式，推動 AI 輔助應用程式現代化邁向真正自主的下一步。

---
