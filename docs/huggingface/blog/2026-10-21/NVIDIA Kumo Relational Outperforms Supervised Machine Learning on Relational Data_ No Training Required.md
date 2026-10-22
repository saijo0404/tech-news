# NVIDIA Kumo Relational Outperforms Supervised Machine Learning on Relational Data, No Training Required

- **來源**: Hugging Face
- **發布日期**: 2026-10-21
- **原文連結**: https://huggingface.co/blog/nvidia/kumo-relational

## 核心主題
NVIDIA Kumo Relational 是一款預訓練的關係型基礎模型，無需訓練即可在企業資料庫上進行預測，表現優於傳統監督機器學習。

## 關鍵重點
- 無需任務特定訓練、特徵工程或表格扁平化，只需連接資料庫並描述預測即可
- 在41個任務上15個資料庫的測試中，表現優於監督機器學習模型和專家設計的梯度提升樹管道
- 在SAP SALT企業基準測試中，比AutoGluon集積模型高出8%的MRR，比近期表格基礎模型高出約25%
- 可處理包含500B+行的大型資料庫，並支援人類與代理（agents）共同使用
- 透過NVIDIA的開源GPU原生結構化資料模型庫（structured-data-models）或NVIDIA NIM部署

## 結論
Kumo Relational 是第一個在常見關係型基準上超越監督機器學習的少樣本基礎模型，為結構化資料預測帶來了新的範式，大幅降低預測建模的門檻與時間成本。
---
