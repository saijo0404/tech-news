# How Schrödinger sped up molecular discovery by 4x with AlphaEvolve

- **來源**: Google Cloud Blog AI & Machine Learning
- **發布日期**: 2026-07-01
- **原文連結**: https://cloud.google.com/blog/products/ai-machine-learning/schrodinger-alphaevolve-molecular-discovery-accelerates-4x/

## 核心主題
Schrödinger 與 Google Cloud 合作使用 AlphaEvolve（由 Google DeepMind 開發的演化 AI 編碼代理）來優化其機器學習力場（MLFF）訓練管道，成功將分子發現速度提升 4 倍。

## 關鍵重點
- Schrödinger 識別出兩個限制性能的關鍵演算法：鄰居列表計算和 Ewald 求和，其中 Ewald 求和是主要性能瓶頸。
- 通過將簡單的 for-loops 替換為並行批次矩陣乘法，程序成功率從不到 1%（40/5000）提升至 60% 以上。
- 性能指標從基準 7.9 提升至近 30，實現 4 倍加速，大幅縮短藥物發現、催化劑設計和材料開發的研發週期。

## 結論
AlphaEvolve 讓 Schrödinger 能夠探索更大的化學空間，更快速、更高效地進行分子篩選，使企業能在數天而非數月內完成分子候選品的篩選，具有重大的商業影響。

---