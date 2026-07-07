# Introducing TabFM: A zero-shot foundation model for tabular data

- **來源**: Google Research Blog
- **發布日期**: 2026-06-30
- **原文連結**: https://research.google/blog/introducing-tabfm-a-zero-shot-foundation-model-for-tabular-data/

## 核心主題
Google 推出 TabFM，一種用於表格數據的零射基礎模型，透過上下文學習方式簡化分類與回歸工作流。

## 關鍵重點
- 使用交替行與列注意力機制處理表格數據，原生捕捉複雜特徵互動
- 透過行壓縮和上下文學習避免傳統訓練流程，無需手動調整超參數或特徵工程
- 完全基於合成數據訓練，可泛化到未見過的真實表格，性能優於傳統監督學習算法
- 預測可在單一前向傳播中完成，無需交叉驗證或模型重訓練

## 結論
TabFM 將表格預測重新定義為上下文學習問題，透過混合注意力架構和大量合成訓練數據，使企業能無需 ML 專業知識即可在 BigQuery 中進行高精度預測，標誌著表格數據處理方式的重大轉變。
---