# How to Govern Autonomous Agents in Enterprise AI Factories

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-29
- **原文連結**: https://developer.nvidia.com/blog/how-to-govern-autonomous-agents-in-enterprise-ai-factories/

## 核心主題
NVIDIA 提出 **Secure Agent Workspace Reference Design**——將使用者裝置（筆電、瀏覽器、IDE）轉為**展示層**而非執行層，讓 AI Agent 在受管理的虛擬機器中執行，透過身份、網路、憑證、政策與人工審核的集中管控，打造企業 AI 工廠中自治代理的安全治理藍圖。

## 關鍵重點
- **兩階段實施架構：從外圍到執行時安全**：①**第一階段——強化外圍防護**——以 VM 作為主要隔離邊界，確保代理活動可觀測、有界且可撤銷。具體措施：為每位使用者配置公司管理的專屬 VM、透過企業 SSO 強制登入關卡、預設阻斷所有網際網路流量僅允許預先核准的內部與外部服務、任何改變系統的代理動作（如合併程式碼或更新工單）需人工審核、所有活動日誌集中匯集供安全團隊監控。②**第二階段——虛擬機器內的執行時安全**——將保護縮短至工具呼叫邊界：使用 **NVIDIA OpenShell** 等專屬執行環境即時監控每項動作、透過中央系統以**簽署安全政策**精確定義代理權限、透過**憑證代理**讓代理接觸短期能力權杖而非原始密碼或 API 金鑰、在每次動作前**自動驗證**安全規則是否生效。
- **Agent 藍圖：可重複的工作流程模板**：藍圖在安全工作空間上執行，每個藍圖配置目標、所需工具、允許服務、資料範圍、寫入權限、審核關卡與日誌期望。開發者從功能最完整的藍圖出發，僅做最小修改來收斂行為。關鍵實踐包括：透過 SSO 註冊代理身份並使用委派紀錄定義權限、使用憑證代理避免硬編碼秘密、透過閘道層管理配額與 RBAC、設定「爆炸半徑」控制並要求所有日誌以 **OCSF 格式**輸出以利稽核。
- **雲端或本端部署：GitOps 驅動的可重複營運**：本端部署使用 **Red Hat OpenShift Virtualization**，雲端部署使用 **Microsoft Azure**。核心模式相同——每個使用者專屬 VM，本地端點僅作為展示表面。部署步驟涵蓋：VM 配置、透過可信存取代理建立路徑、網路邊界管理（OpenShift 使用 NetworkPolicy/EgressFirewall，Azure 使用 Azure Firewall Premium）、VM 映像集中管理、透過 **GitOps** 儲存與同步政策意圖、使用 Workload Identity Federation 與 Azure Key Vault 保護秘密、以及將日誌匯入企業 SIEM（Azure Monitor / Microsoft Sentinel 等）。

## 結論
NVIDIA 的 Secure Agent Workspace 設計揭示了一個核心原則：**自治 AI Agent 的安全不在於信任代理不會出錯，而在於建立一個即使代理出錯也能將損害控制在最小範圍的架構**。從 VM 隔離、網路預設拒絕、政策簽署、憑證代理到 GitOps 驅動的政策治理——每一層都在回答同一個問題：「如果代理做了不該做的事，系統如何阻止它？」這套框架為企業將 AI Agent 從實驗品升級為正式員工級工具提供了可操作的安全路徑。

---
