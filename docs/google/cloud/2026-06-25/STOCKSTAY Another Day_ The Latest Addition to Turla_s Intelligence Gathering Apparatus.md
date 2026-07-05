# STOCKSTAY: Another Day – The Latest Addition to Turla's Intelligence Gathering Apparatus

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-26
- **原文連結**: https://cloud.google.com/blog/topics/threat-intelligence/stockstay-turla-intelligence-gathering/

## 核心主題
Google Threat Intelligence Group（GTIG）深入分析由俄羅斯關聯的 Turla 組織開發的 .NET 後門木馬 STOCKSTAY，揭示其自 2022 年底以來如何演進為高度模組化、反偵測能力成熟的網路間諔工具，主要針對烏克蘭防務與義大利外交部相關實體。

## 關鍵重點
- **三層模組化架構與多層次反偵測**：STOCKSTAY 採用 STOCKBROKER（通訊中繼）、STOCKMARKET（任務協調）與 STOCKTRADER（後門執行）分工架構，偽裝成股票市場數據工具。結合環境錨定（以主機名稱或網域雜湊加密配置）、K1MORPHER 字串混淆技術（基於 Squirrel3 RNG），以及將功能拆分為偽造 Windows 系統檔的 DLL，展現極高的反分析與持久化能力。
- **複雜部署鏈與精準誘餌演化**：從 2023 年單一執行檔演進至 2025 年多階段投放，攻擊者靈活運用惡意 RDP 檔案、HTA 腳本、WinRAR 路徑遍歷漏洞（CVE-2025-8088）與受入侵 WordPress 網站進行分發。誘餌高度情境化，包含烏克蘭大學通知、軍事人員現金福利計算機、無人機（UAV）狀態報告與外交選舉主題，並透過外部圖片引用偵測文件是否被開啟。
- **高信心度歸因與完整偵測規則**：GTIG 以高信心度將 STOCKSTAY 歸因於 Turla，關鍵證據包括共用 K1MORPHER 混淆技術、Windows-1251 編碼使用、與 KAZUAR 共享受入侵基礎設施，以及在 Mandiant 事件回應中與 WILDDAY、DIAMONDBACK 等專有工具一併部署。GTIG 同步發布涵蓋配置檔、加密容器、各組件方法名稱、K1MORPHER 混淆的完整 YARA 規則集，將部署至 Google SecOps 與 Mandiant Frontline 供全球客戶即時防護。

## 結論
STOCKSTAY 不僅是 Turla 武器庫的新成員，更是其逾二十年網路間諜經驗的技術集大成者。從模組化架構設計、環境錨定與混淆技術的持續迭代，到針對東歐與歐洲外交防務領域的精準誘餌投放，每一項設計都體現了頂級 APT 組織對防禦機制的深刻理解。GTIG 的完整時間軸、IOCs 與 YARA 偵測規則為安全社群提供了關鍵的狩獵指標，大幅強化了識別與阻斷 Turla 間諜活動的防禦能力。

---
