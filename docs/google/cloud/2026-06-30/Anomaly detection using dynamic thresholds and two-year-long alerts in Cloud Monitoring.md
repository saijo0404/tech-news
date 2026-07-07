# Cloud Monitoring adds long-lookback alert policies for PromQL

- **來源**: Google Cloud Blog
- **發布日期**: 2026-07-01
- **原文連結**: https://cloud.google.com/blog/products/management-tools/cloud-monitoring-adds-long-lookback-alert-policies-for-promql/

## 核心主題
Google Cloud Monitoring 推出支援兩年期數據的長遠回查警報政策，並引入動態閾值功能，解決傳統靜態閾值無法適應變化數據的問題。

## 關鍵重點
- 支援兩年期數據分析，可進行年際與季際比較，解決單一靜態閾值無法捕捉時間性異常的問題
- 動態閾值允許警報基於歷史數據而非固定數值，例如「最近 5 分鐘平均值是過去一週平均值的 2 倍」
- 提供三種動態閾值算法：移動平均（適合穩定數據）、Z-score 分數（適合波動數據）、季節分解（適合時間模式明顯的數據）
- 可應用於防止雲端服務費用失控等場景，例如當 AI token 使用量異常激增時自動觸發警報

## 結論
此功能讓警報策略更具彈性，能自動適應工作負載變化，降低管理成本，並提供早期預警以控制潛在風險。
---
