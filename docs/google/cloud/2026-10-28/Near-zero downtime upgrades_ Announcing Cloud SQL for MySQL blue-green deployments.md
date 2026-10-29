# Near-zero downtime upgrades: Announcing Cloud SQL for MySQL blue-green deployments

- **來源**: Google Cloud Blog
- **發布日期**: 2026-10-29
- **原文連結**: https://cloud.google.com/blog/products/databases/cloud-sql-blue-green-deployments/

## 核心主題
Google Cloud 推出 Cloud SQL for MySQL 的藍綠部署功能，實現近乎零停機的資料庫升級，讓企業無需犧牲週末也能安全升級資料庫版本。

## 關鍵重點
- **近乎零停機切換**：使用 Cloud SQL Enterprise Plus 的组织可實現毫秒級停機，切換過程極速
- **無需修改應用程式**：切換時自動轉移資料庫 IP 地址、實例名稱和備份，開發者無需重新撰寫連接字串或修改配置
- **安全實數據測試**：可在升級後的綠色環境中運行實際應用程式流量和查詢進行驗證，如有問題可隨時取消升級而不影響生產資料庫

## 結論
此功能將資料庫升級從高風險的週末專案轉變為可預測的低停機操作，讓團隊能跟上安全週期、釋放最新 AI 引擎功能，並專注於推動業務增長的功能開發。

---