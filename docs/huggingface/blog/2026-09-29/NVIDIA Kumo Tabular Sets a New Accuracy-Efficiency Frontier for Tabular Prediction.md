# NVIDIA Kumo Tabular Sets a New Accuracy-Efficiency Frontier for Tabular Prediction

- **來源**: Hugging Face Blog
- **發布日期**: 2026-09-29
- **原文連結**: https://huggingface.co/blog/nvidia/kumo-tabular

## 核心主題
NVIDIA 推出開源基礎模型 Kumo Tabular，專為表格數據設計，可在單一前向傳播中完成分類與回歸預測，無需訓練、調參或特徵工程。

## 關鍵重點
- **開源與商用授權**：模型以 OpenMDW-1.1 授權發布，可在 Hugging Face 下載，並提供 GitHub 程式碼庫
- **三套模型大小**：提供 28M、71M、137M 參數三種版本，適用於不同規模的表格預測任務
- **首創精度效率 frontier**：在 TabArena、BeyondArena、TALENT、ScoringBench 四個 benchmark 上均排名第一，比 LimiX-2 快 17 倍
- **完全基於人工數據訓練**：模型僅在人工生成的表格上訓練，無需真實數據，具備處理缺失值、異常值等雜訊的能力
- **無需特徵工程**：透過列嵌入、行嵌入與情境學習（in-context learning）架構，直接從標記表格中預測新行標籤

## 結論
NVIDIA Kumo Tabular 標誌著表格數據預測的新一代技術突破，將大語言模型在文本任務上的「零樣本學習」能力應用於表格數據，為企業機器學習提供全新范式。

---