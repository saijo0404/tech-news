# NVIDIA and AWS Collaborate to Bring AI to Production at Scale

- **來源**: NVIDIA Blogs
- **發布日期**: 2026-06-24
- **原文連結**: https://blogs.nvidia.com/blog/nvidia-aws-ai-production-scale/

## 核心主題
NVIDIA 與 AWS 深化合作，透過三大基礎建設創新——Amazon EC2 G7 實例（搭載 NVIDIA RTX PRO 4500 Blackwell）、OpenSearch Serverless 內建 cuVS GPU 加速向量搜尋，以及 AWS 達成 GB300 NVIDIA Exemplar Cloud 認證——提供企業從訓練到推論的端到端 AI 生產規模部署路徑。

## 關鍵重點
- **EC2 G7 實例：Blackwell 多工作負載 GPU 進入 AWS**：EC2 G7 實例搭載 NVIDIA RTX PRO 4500 Blackwell Server Edition GPU，相較 G6 提供最高 4.6 倍 AI 推論效能、2.1 倍繪圖效能，以及使用 cuDF 於 Apache Spark 的顯著加速 GPU 加速數據分析。支援最多 8 顆 GPU、256GB GPU 記憶體、700 Gbps EFA 網路與 7.6TB 本機 NVMe SSD，提供單顆、兩顆、四顆與八顆 GPU 配置（裸機版本即將推出），讓客戶能精確匹配工作負載需求而非過度準備。適用場景涵蓋低延遲推論、高解析度影片工作流、CAD/虛擬桌面/空間計算、以及向量資料庫數據分析。
- **cuVS 成為 OpenSearch Serverless 預設向量搜尋引擎**：新一代 OpenSearch Serverless 將 NVIDIA cuVS 加速向量索引設為所有向量集合的預設計算選項，無需基礎設施管理。向量索引速度較 CPU 單一方案提升達 10 倍，成本僅為四分之一，十億級向量資料庫可在一小時內建完。這將 GPU 向量搜尋從特殊優化專案轉為標準 AWS 功能，並搭配 Serverless 自動縮放減少閒置時的營運負擔。
- **AWS 達成 GB300 NVIDIA Exemplar Cloud 認證**：AWS 在 GB300 上達成了 NVIDIA Exemplar Cloud 等級，表示其訓練效能通過 NVIDIA 基準架構的嚴格性能閾值。此認證由 AWS 與 NVIDIA 深度共同工程實現，讓開發者能信賴一致的硬體層級效能，協助評估雲端供應商、改善總體擁有成本，並加速 AI 專案從規劃到生產的轉換。

## 結論
NVIDIA 與 AWS 的合作覆蓋 AI 基礎建設堆疊的每一層——從 GB300 大規模訓練、EC2 G7 多用途推論與圖形、到 OpenSearch cuVS 預設向量搜尋——核心一致：提供規模化的生產級 AI 基礎設施，且不增加營運團隊的負擔。對於尋求從原型邁向生產規模的企業而言，這套整合方案縮短了從原始資料到可部署 AI 搜尋基礎設施的路徑。

---
