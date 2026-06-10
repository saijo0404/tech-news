# 以 NVIDIA DGX Spark 企業管理功能交付大規模 AI 基礎設施的生命週期控制

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-09
- **原文連結**: https://developer.nvidia.com/blog/delivering-lifecycle-control-for-ai-infrastructure-at-scale-with-nvidia-dgx-spark-enterprise-manageability/

## 核心主題
NVIDIA DGX Spark 與 GB10 系統推出全新「企業管理功能」（Enterprise Manageability），為企業 IT 團隊提供從首次部署到終端退役的完整運作業框架——以無代理 SSH 執行與標準 JSON 輸出設計，整合至現有 CMDB、SIEM 與監控管線，並支援完全斷網（air-gapped）部署。

## 關鍵重點
- **六階段生命週期管理：從採購驗收到終端退役的完整企業框架**：DGX Spark 管理框架以模組化堆疊設計，整合至企業 IT 團隊已有的工具（Progress Chef、Perforce Puppet、Canonical Landscape 等合作夥伴支援），以無代理 SSH 執行搭配有界標準 JSON 輸出——（1）採購與收貨：捕捉穩定裝置識別碼、序號與收貨硬體快照供 CMDB 使用；（2）初始設定：基線硬體、韌體、驅動與軟體庫存、SSH 可達性、入會元資料；（3）持續監控：連續健康檢查、與基線比對的漂移偵測、重置原因分析；（4）維護時段：在變更窗口內進行控制性更新與重啟編排，含分階段部署與回滾安全；（5）事件回應：目標化 L1 分診或完整 L2 診斷套件收集以供升級；（6）終端/遞補與重新部署：具託運鏈證據的出廠重置、退役文件；框架有意區隔「收集器」（唯讀、無特權、安全頻繁執行）與「控制器」（改變狀態、以最小權限 sudo 保護、需變更管理核准）。
- **三大核心工具：診斷、更新協調與客製化安裝應對斷網挑戰**：（1）診斷工具——`spark_diagctl.py` 為主要遠端 SSH 診斷工具，提供 L1 健康狀態（快速 JSON 摘要涵蓋硬碟、網路、驅動）與 L2 深層證據套件（GPU 遙測、核心日誌、硬體事件、PCIe 狀態、韌體資訊與崩潰診斷）；`reset_reason_reporter.py` 透過關聯多個證據來源（系統事件日誌、BMC 紀錄、kernel oops、韌體事件）產生結構化根本原因評估；（2）更新控制面——`spark_updatectl.py` 以 JSON 報告系統更新狀態，支援分階段部署、更新前/後檢查與韌體回滾可視性；（3）客製化安裝——DGX Spark Custom Installation 允許 IT 團隊預先配置裝置（無需執行開機體驗）、從 USB 或本機伺服器自訂軟體後首次開機，支援連線與完全斷網環境，底層依賴 cloud-init、OEM Data 分割區與設定 hook 腳本。
- **企業級安全與合規：從驗證啟動到託運鏈退役的全方位保護**：DGX Spark 管理框架將安全視為一等需求——驗證啟動完整性（Secure Boot 與 verified boot 訊號，每次執行產生證據）、靜態資料加密狀態報告（符合 180-365+ 天稽核保留要求）、APT 套件簽署驗證（發出 PASS/FAIL/UNKNOWN 結果）、出廠重置具託運鏈文件（含方法、時間戳記與成敗狀態，適合監管處置或重新部署工作流）、UEFI 資產元資料標籤（可選，將持久化資產元資料寫入 UEFI 儲存）。RBAC 設計反映最小權限模型，收集器工具無需提升特權，控制器工具需明確 sudo 授權；Canonical Landscape 整合讓已使用 Ubuntu 企業管理的組織可將 DGX Spark 納入同一運作業視圖。

## 結論
NVIDIA DGX Spark Enterprise Manageability 反映了 AI 基礎設施從「開發原型」邁向「企業生產」的關鍵轉變——企業 IT 團隊不再接受與傳統基礎設施不同的標準，他們要求 AI 系統具備同樣的部署、可觀測、安全與管理能力；透過無代理 SSH 設計、標準 JSON 輸出、六大生命週期階段、三大核心工具（診斷、更新、客製化安裝）與企業級安全合規框架，NVIDIA 讓 DGX Spark 能直接融入現有 IT 工作流程（Ansible、Tanium、Landscape 等），無需建立獨立的管理層；特別值得關注的是對完全斷網（air-gapped）部署的全面支援——從客製化安裝到韌體鏡像，這讓高度資安要求的組織（如金融、政府）也能將 AI 基礎設施納入企業級管理；隨著 AI 系統從實驗室走向企業核心，DGX Spark 的管理功能為 AI 基礎設施的運營業成熟度設立了新的企業標準。
