# The OlmoEarth Platform: Geospatial inference at planetary scale

- **來源**: Hugging Face
- **發布日期**: 2026-07-28
- **原文連結**: https://huggingface.co/blog/allenai/olmoearth-infrastructure

## 核心主題
介紹了 OlmoEarth Platform 如何讓地球觀測基礎模型能夠在行星規模上進行高效推理，解決環境組織在基礎模型推理基礎設施上的缺口。

## 關鍵重點
- 平台可處理數十 TB 衛星影像，成本僅每平方公里幾分錢，可在一天內完成大陸規模的推理
- 採用三階段硬體分配策略：資料預處理用 CPU、推理用 GPU、後處理用 CPU，確保 GPU 充分利用
- 單一請求可動員數千個計算實例，北美 wildfire 風險圖例實現 155 倍加速（從 4,737 小時縮短至 30.5 小時）
- 建立自有元數據索引以處理大量衛星影像查詢，避免衝擊外部服務
- 自動處理失敗機制，可重新執行失敗任務，確保系統可靠性

## 結論
OlmoEarth Platform 填補了環境組織在基礎模型推理基礎設施上的缺口，使更多組織能夠利用地球觀測 AI 模型進行森林監測、糧食安全與野火風險等應用，縮小技術資源與實際需求之間的差距。
---
