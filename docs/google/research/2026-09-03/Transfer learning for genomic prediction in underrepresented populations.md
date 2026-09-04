# Transfer learning for genomic prediction in underrepresented populations

- **來源**: Google Research Blog
- **發布日期**: 2026-09-03
- **原文連結**: https://research.google/blog/transfer-learning-for-genomic-prediction-in-underrepresented-populations/

## 核心主題
本研究評估了跨族群遺傳風險預測（PRS）的表現，發現從歐洲族群數據轉移學習在小樣本族群中提升預測準確性，但當目標族群樣本量增加時，準確性反而會下降。

## 關鍵重點
- **樣本量關鍵閾值**：當目標族群樣本量小於 15,000 時，從歐洲數據（UK Biobank）轉移學習能提供統計提升；超過此閾值後，轉移學習反而會降低預測準確性。
- **遺傳架構差異影響**：遺傳保守特徵（如 BMI）能從外部數據受益至更大樣本量（25-40k+），而族群特定特徵（如血脂、血糖）則受益較少。
- **方法比較**：跨族群 Meta-analysis 對族群特定特徵有顯著優勢，而 PRS-CSx 需要更多目標族群數據才能超越簡單方法。
- **臨床意義**：優化多樣族群的預測表現需要擴展本地多樣族群生物庫，並根據特徵遺傳力和樣本量選擇合適的建模策略。

## 結論
本研究提供了系統性的實證指導，強調在跨族群遺傳風險預測中，單純增加外部族群數據並非總是有益，需根據目標族群樣本量大小與特徵遺傳架構選擇最適合的建模方法。

---