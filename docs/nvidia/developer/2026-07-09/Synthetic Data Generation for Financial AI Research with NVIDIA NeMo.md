# Synthetic Data Generation for Financial AI Research with NVIDIA NeMo

- **來源**: developer.nvidia.com/blog
- **發布日期**: 2026-07-09
- **原文連結**: https://developer.nvidia.com/blog/synthetic-data-generation-for-financial-ai-research-with-nvidia-nemo/

## 核心主題
這篇文章介紹了如何使用 NVIDIA NeMo 工具生成大量獨立的金融新聞標題，解決真實數據不平衡問題，並建立可重複的迭代數據生成流程。

## 關鍵重點
- 使用 NeMo Data Designer、NeMo Curator 和 Nemotron 模型，經 82 次迭代生成 502,536 個獨立的金融新聞標題，涵蓋 13 個類別
- 採用「生成→過濾→去重→選擇少樣本→校正分佈」的循環機制，實現約 82% 的語義去重率，確保稀有事件覆蓋
- 在單一 8-way NVIDIA B200 節點上完成，約 6 天運算時間，生成的數據集支援模型蒸馏與分類等下游任務

## 結論
透過迭代式合成數據生成流程，成功填補金融 NLP 訓練數據缺口，為交易研究、風險建模與監控系統提供高品質、多樣化的訓練數據。

---
