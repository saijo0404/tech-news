# Impactful scheduling for GPU clusters

- **來源**: Hugging Face Blog
- **發布日期**: 2026-10-09
- **原文連結**: https://huggingface.co/blog/allenai/impactful-scheduling

## 核心主題
Google Docs 推出了新的 GPU 集群調度器（Asta），解決了 GPU 資源分配中的三大問題，顯著提升了資源利用率和研究項目公平性。

## 關鍵重點
- 引入 GPU 時間預算機制，取代傳統的優先級排程，解決 GPU「佔地」問題
- 層級公平共享排程器根據研究項目結構分配 GPU 時間，提高資源分配公平性
- 排程合約要求工作聲明最小運行時間，並配合自動化維修減少人工介入 74%
- 性能提升顯著：Debug workload 等待時間從 6 小時降至 5 分鐘，整體中位數等待時間從 5 分鐘降至 24 秒
- 30 天測試期間團隊獲得 98% 應得 GPU 時間，13/15 團隊分配達 95% 以上

## 結論
透過透明預算管理取代個案操作，Asta 成功實現了 GPU 資源的高效分配與公平共享，大幅降低調度成本並提升研究項目參與度。