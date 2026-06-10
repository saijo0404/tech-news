# Managed Service for Apache Spark 叢集新功能總覽

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-04
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/enhancements-to-managed-service-for-apache-spark-clusters/

## 核心主題
Google Cloud 宣布 Dataproc 服務正式更名為「Managed Service for Apache Spark」，並針對 Managed Clusters 部署模式推出多項重大更新，涵蓋 Lightning Engine 原生執行引擎、彈性 VM 資源調度、零縮放叢集、MCP Server AI 整合與 Data Agent Kit，全面提升 Spark 效能、操作便利性與 AI 開發體驗。

## 關鍵重點
- **Lightning Engine 原生執行引擎帶來最高 4.9 倍效能提升**：基於 Velox 與 Gluten 打造的 C++ 向量化執行引擎，繞過 JVM 執行瓶頸，將查詢計畫編譯為優化 SIMD 向量化的原生指令，標準開放原始碼 Spark 比較下可達最高 4.9 倍效能提升，並提供領先競爭對手兩倍的性價比；且無需修改現有 Spark 應用程式程式碼即可啟用，直接在建立叢集時勾選 Lightning Engine 選項即可套用。
- **彈性 VM（Flexible VMs）、零縮放叢集與定時停止強化資源與成本管理**：彈性 VM 允許為主節點與工作節點定義最多十種排名的機器類型，搭配自動區域置放掃描以最佳化容量取得並降低 Spot VM 成本；零縮放叢集僅保留主節點維持中繼資料，當無處理工作時可自動縮減至零個工作節點；叢集定時停止則支援依據閒置時間或指定時間自動關機，大幅減少夜間與週末的閒置運算費用。
- **MCP Server 與 Data Agent Kit 打造 AI 驅動資料工程**：Google 推出 Model Context Protocol（MCP）Server 讓 LLM 與 AI 代理程式能使用自然語言安全動態地與 Spark 叢集互動（如建立叢集、提交工作、調整自動縮放策略）；Data Agent Kit 擴充功能讓開發者在 VS Code、Claude Code 或 Codex 等 IDE 中直接以自然語言建構多節點資料管線、進行即時除錯（Gemini Cloud Assist 分析執行器日誌）、輕鬆連線 Spark 資源及管理 Git 與 CI/CD；同時推出 Lakehouse 統一元資料層實現 Spark 與 BigQuery 的讀寫互通，以及 Cluster Image 3.0（內建 Spark 4.1 與 Java 21、支援結構化串流的次秒級即時模式）。

## 結論
Managed Service for Apache Spark 以「更快、更容易、更智慧」三大核心支柱重新定義大資料處理體驗——Lightning Engine 將運算效能推至新高度、彈性資源與 FinOps 功能降低營運門檻、MCP 與 Data Agent Kit 則將生成式 AI 直接嵌入資料工程工作流，搭配 Lakehouse 與 Spark 4.1 即時串流支援，為現代資料團隊提供從資料湖到 AI 代理的完整端到端解決方案。
