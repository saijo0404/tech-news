---
# How Schrödinger sped up molecular discovery by 4x with AlphaEvolve

- **來源**: Google Cloud Blog
- **發布日期**: 2026-06-30
- **原文連結**: https://cloud.google.com/blog/products/ai-machine-learning/schrodinger-alphaevolve-molecular-discovery-accelerates-4x/

## 核心主題
科學軟體公司 Schrödinger 與 Google Cloud 合作，部署 Google DeepMind 的 AlphaEvolve（一種進化式 AI 程式碼代理），自動產生並最佳化分子力場訓練管線中的關鍵算法，將訓練與推論速度提升 **4 倍**。

## 關鍵重點
- **打破計算化學的精度與速度兩難**：傳統上，化學研究者必須在快速但不精確的經典力場，與精確但過於緩慢的量子力學方法之間取捨。機器學習力場（MLFF）透過在量子數據上訓練神經網路來彌合此一缺口，但在處理龐大化學資料庫時仍需更快的處理速度。Schrödinger 鎖定 MLFF 訓練管線中兩個瓶頸算法——**鄰域列表計算**與 **Ewald 求和**（一個計算需求高且原本只能依賴緩慢 for-loop 的關鍵函式）。
- **AlphaEvolve 自動化演算法創新**：AlphaEvolve 迭代產生並改良程式碼，自動將 Ewald 求和從簡單的 for-loop 轉換為使用平行批次矩陣乘法的實作，超越人工編寫的自訂 kernel。經過 5,000 次評估後，程式成功率從不到 1%（40 筆）提升至 **60% 以上**，效能指標從基準分數 7.9 提升至近 30。所有進化後的程式碼都通過了完整測試套件，包括複雜系統（如無序水模型）的回歸測試，確保科學準確性。
- **實際商業影響**：4 倍加速讓分子篩選時間從數月壓縮至數天，直接造福 **藥物發現**（快速識別治療候選藥物）、**觸媒設計**（開發高效化學製程）和 **材料開發**（設計下一代電子與儲能材料）。Schrödinger 未來計劃將此方法擴展至自訂 GPU kernel，測試 AI 產生的程式碼是否能超越人工編寫的實作。

## 結論
AlphaEvolve 的成功證明，進化式 AI 不僅能最佳化軟體效能，更能重新定義科學研究的節奏——當分子篩選從以月計縮短至以日計，藥物發現與材料科學的創新週期將被徹底重塑。這也為「AI 寫 AI 最佳化程式碼」的範式開啟了新的可能性。

---
