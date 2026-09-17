# University of Manchester Uses NVIDIA Earth-2 to Forecast Air Pollution Across the UK

- **來源**: NVIDIA Blog
- **發布日期**: 2026-09-15
- **原文連結**: https://blogs.nvidia.com/blog/uk-air-pollution-research-earth-2/

## 核心主題
曼徹斯特大學研究團隊利用 NVIDIA Earth-2 生成式 AI 模型，成功開發出空氣污染預測系統，解決了傳統化學模型計算成本高昂的問題，使空氣品質預測變得更快、更精確。

## 關鍵重點
- **Earth-2 CorrDiff 模型開發**：研究團隊在英國國家超級電腦 Isambard-AI 上訓練了 Earth-2 CorrDiff 生成式降尺度模型，僅用兩天即可完成訓練，並成功生成 UK 範圍內 2-3 平方公里解析度的詳細空氣污染預測。
- **Earth-2 StormCast 時間依賴預測**：團隊進一步開發了 Earth-2 StormCast 模型，可直接利用空氣品質觀察數據進行時間依賴的預測，並已在 NVIDIA DGX Spark 桌上型 AI 系統上驗證運行。
- **應用場景擴展**：模型可應用於公共健康預警（如向哮喘患者預知未來空氣污染情況）、醫療機構主動空氣品質洞察，以及與邊緣 AI 設備結合實現 wildfire 等事件時的即時決策。
- **開放源碼與全球共享**：團隊計劃開放訓練數據和工作流程，讓其他國家和地區也能利用類似模型訓練自己的空氣污染預測系統，降低 AI 模型開發門檻。

## 結論
這項研究展示了 NVIDIA Earth-2 框架在科學領域的巨大潛力，不僅大幅降低了空氣污染預測的計算成本，還為全球公共健康和環境管理提供了可複製的解決方案。未來，隨著更多開放源碼和更簡單的代理介面，這項技術有望被更多國家和地區採用，實現更廣泛的空氣品質監測與預警。
---
