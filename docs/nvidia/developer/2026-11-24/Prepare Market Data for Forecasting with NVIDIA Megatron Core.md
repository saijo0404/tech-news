# Prepare Market Data for Forecasting with NVIDIA Megatron Core

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-11-24
- **原文連結**: https://developer.nvidia.com/blog/prepare-market-data-for-forecasting-with-nvidia-megatron-core/

## 核心主題
這篇文章介紹如何使用 NVIDIA Megatron Core 庫來預備市場數據，用於金融時間序列預測。

## 關鍵重點
- 使用 Megatron-LM 庫和預配置訓練腳本，將內盤市場棒狀數據轉換為模型準備好的張量
- 預處理管道通過分組連續棒狀數據、滑動固定長度上下文窗口，計算多時間點的預測目標（回報率與交易量）
- 記憶體映射數據載入器在每個張量並行組內共享批次，實現高效分佈式訓練
- 時間保障措施將數據按日期分割，設置禁售期防止跨分割洩漏，並僅使用訓練集計算目標統計量
- 框架將數據接口與模型架構分離，允許研究人員替換自訂預測模型而重用水預備邏輯

## 結論
這是一個可重用的數據預備框架，允許研究人員使用自己的市場棒狀 Parquet 文件來準備數據集並運行訓練實驗，同時保持數據層不變以替換預測模型架構。

---