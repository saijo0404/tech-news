# 使用 Google Cloud Storage MCP Server 連接 AI 代理與非結構化資料

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-02
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/build-ai-agents-faster-with-gcs-google-cloud-storage-mcp-server/

## 核心主題
Google Cloud 推出 GCS（Google Cloud Storage）MCP Server，讓 AI 代理能安全標準化地存取非結構化資料，結合 Remote（受管）與 Local（自管）兩種模式，以及客戶實際應用案例（Palo Alto Networks、Airwallex、Snap），展現 GCS 作為現代 AI 代理技術堆疊基礎建設的關鍵角色。

## 關鍵重點
- **三大客戶實戰案例：從網路安全到資料科學效率飛躍**：Palo Alto Networks 的 Strata Co-Pilot 代理以 GCS 作為「歷史記憶」，透過 Gemini Live API 引導網路安全管理員完成複雜設定流程；Airwallex 的 AI Assistant 利用 GCS 儲存費用政策文件與擷取資訊，自動產生審核管線將原本需數小時的任務自動化；Snap 的 Job Optimization Agent 分析儲存於 GCS 的數千個 Flink 與 Spark 工作規格、元資料與歷史指標，將調查時間從 30 分鐘縮短至 30 秒，三者皆由 GCS MCP Server 處理資料操作並執行標準 RBAC 存取政策。
- **Remote MCP Server（受管）與 Local MCP Server（自管）雙軌選擇**：Remote Server 為完全受管方案，零基礎建設部署即可連線 GCS 非結構化資料，與 ADK、Google Antigravity、Claude 等框架與客戶無縫整合，並透過 IAM 身分驗證、Cloud Audit Logs 完整可觀察性及可選的 Model Armor 內容掃描（防提示注入、工具毒化、資洩）；Local Server 為開源方案（GitHub），適用於需自訂商業邏輯（如 PII 脫敏、整合內部系統內容）的情境，現已納入「MCP Toolbox for Databases」單一儲存庫，支援 GCS、BigQuery、AlloyDB、Spanner、Cloud SQL 等多種資料服務。
- **安全治理：身分優先與完整稽核**：GCS MCP Server 以 IAM 取代共享金鑰進行驗證，確保代理僅能存取明確授權的儲存桶與物件；所有請求與動作記錄於 Cloud Audit Logs 供安全團隊追溯；Model Armor 防護常見 MCP 攻擊向量（直接/間接提示注入、工具毒化、惡意 URL/SQL 注入）並防止敏感資料外洩，企業可安心將生產級代理部署於 GCP 標準身分、可觀察性與安全框架之上。

## 結論
GCS MCP Server 將 Google Cloud Storage 從被動的物件儲存轉變為 AI 代理的「主動式智慧庫」，以 Remote/Local 雙模式兼顧快速部署與自訂彈性，結合企業級安全治理，讓開發者能專注於代理創新而非基礎建設排障——非結構化資料不再是代理的挑戰，而是其最大的資產。
