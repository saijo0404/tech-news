# 以 Google Security Operations 代理偵測並遏制 AI 驅動的威脅

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-09
- **原文連結**: https://cloud.google.com/blog/products/identity-security/detecting-and-containing-powered-threats-with-google-security-operations-agents/

## 核心主題
Google Cloud 揭示 Google Security Operations 如何與 AI Threat Defense 協同運作，透過 Gemini 原生的三大專門代理——檢測工程代理、分類與調查代理、威脅獵捕代理——以機器規模與機器速度實現自動化的威脅偵測、調查、隔離與回應，即使面對無法修補的漏洞與零日攻擊也能維持防禦韌性。

## 關鍵重點
- **修補差距危機：M-Trends 2026 顯示漏洞利用時間縮短至負七天，Verizon DBIR 顯示 KEV 列表漏洞修復率僅 26%**：AI 加速威脅行為者讓防禦面臨前所未有挑戰，根據 M-Trends 2026，漏洞利用已成為最常見的初始感染向量，平均利用時間縮短至負七天——意味著exploit 常在官方修補程式發布前就已發生；2026 Verizon DBIR 涵蓋逾 13,000 家組織的調查顯示，CISA 已知被利用漏洞（KEV）列表中僅 26% 已完全修復，從偵測到完全修補的中位數耗時達 43 天；Google Security Operations 透過三大能力填補此一關鍵弱點：（1）持續自主覆蓋分析與檢測生成：Detection Engineering 代理可自動將未修補漏洞的新型利用模式轉化為自訂檢測規則，整合 Google 威脅情報（Mandiant 新興威脅、紅隊報告、自主惡意軟體分析等）與內部安全遙測，以合成事件驗證新規則確保漏洞被覆蓋；（2）自主調查、隔離與回應：Triage and Investigation 代理（一般可用）已調查超過 500 萬筆警示，將傳統 30 分鐘手動分析縮短至 60 秒，並結合動態 AI 代理與確定性企業 Playbook 的混合方法（Agentic automation，預覽中）實現快速隔離；（3）回溯獵捕：Threat Hunting 代理（預覽中）掃瞄企業數 PB 的遥測數據（包括歷史日誌），從被動反應轉向深度主動的威脅獵捕。
- **Axios 供應鏈攻擊案例：Detection Engineering 代理揭示殺手鏈盲點並自動工程化 YARA-L 規則**：當行為者可零邊際成本生成獨特 exploit 與命令控制（C2）基礎設施時，靜態指標如雜湊值與 IP 瞬間失效，防禦者必須檢測攻擊的行為戰術、技術與程序（TTP）；Google 使用 Detection Engineering 代理審查 Axios 供應鏈攻擊（UNC1069）的覆蓋率——代理將行動情報映射為行為威脅檢測機會（TDO）、使用高保真合成 UDM 日誌模擬攻擊鏈並對活躍規則進行測試——成功標記出中間階段（重命名的 PowerShell 與 macOS 背景 shell）的執行，但在初始入口點（NPM postinstall dropper）與最終 C2 退出點處於盲區；此結果幫助 Google 主動工程化自訂 YARA-L 規則以填補殺手鏈首尾的覆蓋缺口。
- **機器速度防禦實現 70% 降低漏洞風險與成本：從被動告警到主動韌性的防禦典範轉移**：Google Security Operations 以機器規模與速度交付三大能力——從持續自主覆蓋分析（Detection Engineering 自動翻譯新型利用模式為環境自訂規則並以合成事件驗證）、自主調查與回應（Triage 代理整合雲端與企業資產可視性，將分散訊號轉為完整、可操作的敘事，30 分鐘分析壓縮至 60 秒）、回溯獵捕（Threat Hunting 代理掃瞄數 PB 數據發現傳統防禦遺漏的隱蔽威脅）——結合 Google AI Threat Defense 的準備、掃描與優先排序、修復、監控四步框架，以 AI 對抗 AI，最終實現 70% 的漏洞風險與成本降低，讓組織在主要控制失效時仍能維持防禦韌性。

## 結論
Google Security Operations 的 Gemini 原生專門代理代表了安全營運中心從「人力密集型告警處理」到「機器速度自主防禦」的根本轉變——Detection Engineering 代理在修補差距出現前自動生成檢測規則、Triage and Investigation 代理將 30 分鐘分析壓縮至 60 秒並減少誤報干擾、Threat Hunting 代理以回溯獵捕捕捉繞過前沿控制的隱蔽威脅；在 M-Trends 2026 揭示漏洞利用時間已縮短至負七天的時代，以 AI 驅動威脅行為者的攻擊速度已經超越人力防禦的反應能力，Google 以三大代理構建的自主平台讓安全團隊能在修補前、修補中、甚至攻擊成功後仍能維持操作韌性，實現 70% 的風險與成本降低。
