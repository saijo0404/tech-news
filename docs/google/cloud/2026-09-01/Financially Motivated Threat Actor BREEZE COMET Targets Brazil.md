# Financially Motivated Threat Actor BREEZE COMET Targets Brazil

- **來源**: Google Cloud Blog
- **發布日期**: 2026-09-01
- **原文連結**: https://cloud.google.com/blog/topics/threat-intelligence/financially-motivated-threat-actor-breeze-comet-targets-brazil/

## 核心主題
BREEZE COMET 威脅組織針對巴西金融系統發動攻擊，使用多種後門工具與 AI 輔助技術進行詐騙。

## 關鍵重點
- **攻擊手法**：使用密碼噴灑、聲望呼叫、受控巴西政府網站作為階梯進行初始入侵
- **後門工具**：部署 XWORM、LIGHTPAINT、MILDFROST、KICKPLATE、BOATBEAM 等多種自訂後門工具
- **攻擊成效**：成功執行數千美元資產詐騙交易，並清除事件記錄以掩蓋痕跡
- **緩解措施**：實施應用控制、網路微隔離、Secrets 管理及 Google SecOps 檢測規則

## 結論
建議實施多層防護措施，包括網路微隔離、Kubernetes 隔離、集中式 Secrets 管理以及部署針對 BREEZE COMET 威脅的 YARA Rules 檢測規則，以有效應對財務動機威脅組織的攻擊。

---