# Get Started with GPU-Accelerated DuckDB Analytics Using the Sirius Core Extension

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-11-23
- **原文連結**: https://developer.nvidia.com/blog/get-started-with-gpu-accelerated-duckdb-analytics-using-the-sirius-core-extension/

## 核心主題
這篇文章介紹了 NVIDIA 與 DuckLabs 合作推出的 Sirius 核心擴展，它是一個 GPU 本地的 SQL 引擎，可以作為 DuckDB 的核心擴展，讓使用者無需修改 SQL 語法即可在 NVIDIA GPU 上執行分析查詢，並帶來顯著的性能提升。

## 關鍵重點
- Sirius 透過兩個 SQL 指令（INSTALL sirius 和 LOAD sirius）即可安裝並啟用，無需重新撰寫 SQL 或改變資料結構。
- 測試顯示，使用優化後的雙 GPU 配置，在 TPC-H 查詢上可獲得 3.25 至 5.50 倍的加速效果，並降低最多 79% 的查詢時間計算成本。
- DuckDB 負責解析和優化查詢，而 Sirius 則在 GPU 上執行支援的查詢計劃，不支援的功能會自動回退到 CPU 引擎。

## 結論
Sirius 為 DuckDB 使用者提供了無需修改現有工作流程即可利用 GPU 加速分析查詢的解決方案，特別適合處理大規模資料集，可顯著提升查詢效率並降低計算成本。
---