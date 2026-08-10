# Zero-code, low-cost data ingestion: New BigQuery DTS capabilities

- **來源**: Google Cloud Blog
- **發布日期**: 2026-08-08
- **原文連結**: https://cloud.google.com/blog/products/data-analytics/new-bigquery-data-transfer-service-capabilities/

## 核心主題
BigQuery Data Transfer Service (DTS) 推出新功能，提供零程式碼、低成本的數據導入解決方案，並擴展了新的連接器支援。

## 關鍵重點
- **Open Lakehouse 導入**: 支援直接導入 Apache Iceberg 管理表，可從 Google Cloud Storage、Amazon S3 和 Azure Blob Storage 直接導入，實現多雲端儲存相容性。
- **新一代代理架構**: 推出完全管理的遠端 Model Context Protocol (MCP) 伺服器，讓開發者能程式化發現數據來源並自動配置/執行數據傳輸。
- **企業與關係型資料庫**: 新增 Microsoft SQL Server (預覽)、PostgreSQL (GA) 和 MySQL (GA) 支援，支援全量或增量傳輸，可從本地環境、CloudSQL 和其他雲端複製數據。
- **電商與成長行銷平台**: 新增 Shopify、Klaviyo、HubSpot 和 Mailchimp 連接器，自動提取訂單歷史、庫存日誌、客戶資料、郵件/SMS 互動日誌等。
- **遷移連接器**: Snowflake (GA) 支援增量傳輸、自動架構偵測和私有連接性，可遷移 Google Cloud、AWS 和 Azure 上的數據。
- **主要連接器增強**: ServiceNow、Salesforce 和 Oracle 連接器新增原生增量更新支援，加速大型管道刷新。
- **零成本數據導入**: Google 內部來源（除 Google Play 外）免費導入，Amazon S3、Azure Blob Storage、Amazon Redshift 和 Teradata 也免費；第三方 SaaS 採用靈活消費模式，計算費用低於每小時 6 美分。
- **無縫安全性與原生管理**: 完全整合 Cloud IAM，自動繼承目標數據集的列級別安全、行級別安全和客戶管理加密鍵，無需額外配置。
- **業界領先的性能與韌性**: 承諾 >=99.99% 月服務時效，確保分析、自動化管道和運營儀表板可靠更新。

## 結論
BigQuery DTS 透過零程式碼自動化、低成本的數據導入解決方案，幫助企業擺脫繁瑣的 ETL 管道維護，快速轉型至戰略性數據科學，同時提供高安全性、高可用性和多雲端相容性。
---
