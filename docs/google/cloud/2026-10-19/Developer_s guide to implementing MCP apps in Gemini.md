# Developer's guide to implementing MCP apps in Gemini

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-20
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/devs-guide-to-mcp-apps-in-gemini/

## 核心主題
這篇文章介紹了如何在 Gemini Enterprise 中實現 MCP (Model Context Protocol) 應用，通過將工具與即時 UI 結合，解決傳統文本助手在視覺化、多步驟工作場景下的局限性。

## 關鍵重點
- **第三代企業助手**：MCP Apps 是企業助手的第三代進化，將工具與即時工作區結合，調整無需模型輪詢即可執行
- **六項主要優勢**：響應式用戶體驗、專項工作流（如法律審查、3D 查看器）、企業級安全、人工介入治理、開放標準和廣泛連接性
- **三層解耦架構**：客戶端瀏覽器、Gemini Enterprise、Google Cloud (Cloud Run)，各層之間僅與相鄰層通信
- **雙層認證機制**：Layer 1 (Cloud Run IAM) 確保服務權限，Layer 2 (In-App OAuth) 驗證用戶身份
- **七步部署流程**：啟用 API → 部署容器 → 授予權限 → 創建 OAuth 客戶端 → 設置約束 → 啟用動作 → 連接數據庫

## 結論
通過使用 MCP Apps，開發者可以在 Gemini Enterprise 中快速構建專業應用，無需重建基礎設施，同時享受企業級安全和響應式用戶體驗。Gemini 提供 workforce 認證、受管數據訪問和預設助手，而開發者只需在私有的 Cloud Run 服務上託管 MCP 伺服器。
---
