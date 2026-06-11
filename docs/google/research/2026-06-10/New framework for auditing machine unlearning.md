---
# New framework for auditing machine unlearning

- **來源**: Google Research Blog
- **發布日期**: 2026-06-10
- **原文連結**: https://research.google/blog/new-framework-for-auditing-machine-unlearning/

## 核心主題
Google Research 提出「正規化 f-散度核檢定」（Regularized f-Divergence Kernel Tests）框架，以 AISTATS 2026 論文形式發表，透過多種 f-散度度量與三樣本相對距離測試，大幅提升機器學習模型「機器學習消除」（machine unlearning）與差分隱私稽核的靈敏度與準確性。

## 關鍵重點
- **傳統兩樣本檢定的缺陷**：現有稽核方法依賴兩樣本統計檢定，但在大規模模型上因隨機雜訊導致檢定力大幅下降；同時 MMD 等標準工具缺乏局部異常的捕捉能力，且近期研究證明標準局部消除算法無法達到完美「重訓等價」（retrain equivalence），導致兩樣本測試永遠會錯誤標記安全模型為失敗。
- **自适应 f-散度核檢定框架**：新框架整合 Chi-squared、KL 散度（捕捉平滑局部差異）與專為隱私定義設計的 Hockey-stick 散度（可控制統計不可區分度的安全預算閾值），透過核正則化方法在高維資料上高效估計散度，並自動選擇最佳散度與超參數配置，完全消除樣本分割需求。
- **隱私稽核與消除評估實驗成果**：在稀疏向量技術機制（SVT3）的隱私稽核中，新框架僅需數千個樣本就檢測到違規（先前方法需百萬級樣本）；在三樣本相對測試中，所有近似消除方法均未通過嚴格兩樣本定義，只有隨機標籤（random label）技術通過評估，而精細調整（finetuning）、剪枝（pruning）與 Selective Synaptic Dampening 被發現無法真正忘記目標資料。

## 結論
此框架為機器學習行為稽核提供了更精確、更靈活且具數學嚴謹性的分析工具，使研究人員與稽核者能以統計方式證明模型是否存在資料洩漏；未來工作將聚焦於理論化不同任務的最佳散度選擇，以及建立更緊密的樣本複雜度界線以進一步提升稽核效率。

---
