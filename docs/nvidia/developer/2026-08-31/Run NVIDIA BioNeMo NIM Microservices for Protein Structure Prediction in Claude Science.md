# Run NVIDIA BioNeMo NIM Microservices for Protein Structure Prediction in Claude Science

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-08-31
- **原文連結**: https://developer.nvidia.com/blog/run-nvidia-bionemo-nim-microservices-for-protein-structure-prediction-in-claude-science/

## 核心主題
這篇文章介紹了 NVIDIA BioNeMo Agent Toolkit 如何與 Claude Science 整合，讓 AI 代理能夠使用 NVIDIA NIM 微服務進行蛋白質結構預測。文章通過實際案例（Seh1 蛋白質及其潛在伴侶）展示了多序列比對（MSA）對於蛋白質結構預測的重要性。

## 關鍵重點
- NVIDIA BioNeMo Agent Toolkit 將超過十年的 BioNeMo 生命科學模型、庫和工作流打包成可被代理調用的技能，整合到 Claude Science 中，使 AI 代理能夠自動化複雜的科學工作流。
- 通過比較 OpenFold3 和 Boltz-2 兩個模型，文章展示了當使用多序列比對（MSA）輸入時，蛋白質結構預測的介面置信度（iPTM）分別達到 0.85 和 0.82，而沒有 MSA 輸入時則降至 0.14 和 0.19，證明 MSA 是介面預測的關鍵輸入。
- 結構疊加顯示當伴侶存在時，Seh1 的摺疊是完成的而不是被重構的，兩個模型獨立地將相同的 C1HCX1 β-鏈放置在 WD40 扣帶位置，驗證了預測的準確性。

## 結論
NVIDIA BioNeMo Agent Toolkit 與 Claude Science 的整合為科學研究提供了強大的工具，使 AI 代理能夠自動化複雜的蛋白質結構預測工作流。多序列比對（MSA）是蛋白質結構預測，特別是蛋白質複合物介面預測的關鍵輸入，具有決定性的影響。

---