# AlloyDB Omni integration with local models

- **來源**: Google Cloud Blog
- **發布日期**: 2026-11-24
- **原文連結**: https://cloud.google.com/blog/products/databases/alloydb-omni-integration-with-local-models/

## 核心主題
Google 推出 AlloyDB Omni，可與本地部署的大型語言模型（LLM）整合，讓企業能在私有環境中安全地運算 AI，同時保持數據 sovereignty。

## 關鍵重點
- **本地化 AI 部署**：AlloyDB Omni 可下載並部署到任何基礎設施（雲端、數據中心或筆記本電腦），內建 ScaNN 索引技術，支援向量嵌入儲存與自然語言查詢。
- **支援多種本地模型**：可連接 Gemma 4、Qwen3.8 等本地模型，透過 SQL 直接調用模型服務，無需跨網路傳輸數據。
- **數據安全與低延遲**：所有數據與模型都在同一本地環境中運行，避免數據跨公共互聯網，同時減少推理請求的網絡延遲。
- **SQL 原生集成**：支援透過標準 SQL 調用 AI 函數，例如 `ai.generate()`，可將 AI 能力直接嵌入現有數據庫查詢中。
- **快速部署指南**：提供基於 Kubernetes 的完整部署步驟，包括 AlloyDB Omni 操作員、模型註冊與測試示例。

## 結論
AlloyDB Omni 與本地模型的整合為企業提供了在私有環境中安全、低延遲地運算 AI 的能力，特別適合對數據 sovereignty 有嚴格要求的場景。透過 SQL 原生集成，企業可輕鬆將 AI 能力融入現有數據庫工作流，無需複雜的架構變更。
---
