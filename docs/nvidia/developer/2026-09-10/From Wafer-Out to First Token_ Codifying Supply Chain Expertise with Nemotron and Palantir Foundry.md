# From Wafer-Out to First Token: Codifying Supply Chain Expertise with Nemotron and Palantir Foundry

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-09-10
- **原文連結**: https://developer.nvidia.com/blog/from-wafer-out-to-first-token-codifying-supply-chain-expertise-with-nemotron-and-palantir-foundry/

## 核心主題
NVIDIA 利用 Palantir Foundry 建立數位供應鏈智能指揮中心，結合 cuOpt 定量優化與人類專家知識，訓練出專精於供應鏈分配的 Nemotron 3.5 Lightning 模型，實現從晶片出貨到首個 token 的完整供應鏈管理。

## 關鍵重點
- **數位供應鏈指揮中心**：NVIDIA 與 Palantir 合作建立統一視圖，整合材料、產能與定性訊號，透過 Ontology 架構實現供應鏈全貌可視化。
- **cuOpt 定量優化**：使用 NVIDIA cuOpt 解決每週混合整數線性規劃問題，最小化 Time of Ownership (TOO)，識別關鍵約束條件。
- **人類專家優勢**：人類規劃者能整合郵件、天氣預報、地緣政治事件等 cuOpt 無法捕捉的資訊，表現優於數學模型。
- **Nemotron 3.5 Lightning 模型**：基於歷史決策訓練的 30B 參數模型，在開發測試集上達到 86.7% 的分配決策準確率，超越 Nemotron 3 Ultra (55.5%) 及自身基礎模型 (17.5%)。
- **知識飛輪機制**：接受的建議、編輯與覆核結果回饋至 Ontology，支持未來受控再訓練，累積機構知識並縮短上線時間。

## 結論
NVIDIA 透過將人類專家判斷數位化並訓練專精模型，成功將供應鏈決策從每週手動重構轉化為可複現、可累積的機構知識，大幅提升決策準確性與效率，為其他企業提供可複製的供應鏈 AI 應用範式。

---

*本文摘要基於 NVIDIA Technical Blog 於 2026 年 9 月 10 日發表的文章，內容可能不完整，重要資訊請以原文為準。*
