# Safely run AI-generated code in Cloud Run sandboxes

- **來源**: cloud.google.com/blog
- **發布日期**: 2026-07-10
- **原文連結**: https://cloud.google.com/blog/topics/developers-practitioners/google-cloud-run-sandboxes-are-in-public-preview/

## 核心主題
Google Cloud 推出 Cloud Run 沙盒功能，提供輕量級、隔離的執行環境，讓開發者能在安全環境中執行 AI 生成代碼或不可信的二進制，無需額外成本或專用基礎設施。

## 關鍵重點
- Cloud Run 沙盒是原生、安全且超快速的執行環境，啟動速度快（平均 500ms），可在現有 Cloud Run 服務中輕量級地執行不可信代碼
- 核心使用案例包括 LLM 代碼解譯器（執行 Python、R 或 SQL 代碼）、無頭瀏覽器（安全爬蟲和自動化網頁工作流）、以及用戶提交代碼執行
- 安全性設計包含零信任默認、隔離權限（無法訪問環境變數或 Google Cloud 元數據伺服器）、鎖定網絡出站（預設無網絡訪問）以及安全文件系統覆蓋（只讀文件系統視圖，寫入隔離臨時記憶體覆蓋）

## 結論
Cloud Run 沙盒提供零額外成本的安全執行環境，讓企業能安全地讓 AI 生成代碼運行，同時保持對資源和權限的完全控制，適合需要執行不可信代碼的 AI 應用場景。

---
