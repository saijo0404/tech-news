# 推出 North Mini Code：Cohere 首款開發者模型

- **來源**: Hugging Face Blog
- **發布日期**: 2026-06-09
- **原文連結**: https://huggingface.co/blog/CohereLabs/introducing-north-mini-code

## 核心主題
Cohere 發布 North Mini Code，一款 30B 參數（3B 活躍參數）的 MoE 模型，專為代理式軟體工程任務設計，在 Artificial Analysis Coding Index 中表現優於多項同級與更大規模的開源模型。

## 關鍵重點
- **針對代理式編碼優化的訓練流程**：採用兩階段級聯監督微調（SFT）搭配可驗證獎勵的強化學習（RLVR），從 64K 到 128K 的「長到更長」串聯訓練確保高品質程式碼資料不被稀釋；使用 CISPO 目標函數進行異步 RL 訓練，確保長軌跡的梯度訊號不被稀釋。
- **跨工具框架的強大魯棒性**：在第二階段 SFT 中引入多種代理工具框架（SWE-Agent、mini-SWE-agent、OpenCode）的混合數據，僅需 6% 的額外橫向數據即可在 OpenCode 評估中獲得 10% 提升，同時不損害 SWE-Agent 上的表現，顯示不同框架間的技能具有互補性。
- **RLVR 帶來顯著效能躍升**：經強化學習微調後，模型在 Terminal-Bench v2 上 pass@1 絕對提升 7.9%、SWE-Bench Verified 提升 3.0%；人類評估顯示 RLVR 模型在程式碼編輯任務中以 66.1% 勝率超越僅 SFT 的版本，且產生更短的推理軌跡與更少的無效工具呼叫。

## 結論
North Mini Code 作為 Cohere 首款開發者模型，以 30B 參數的體積在代理式編碼任務中展現出超越更大規模競爭對手的效能，其多階段 SFT + RLVR 訓練策略與跨框架魯棒性設計，為開源生態提供了一個高效能的開發者 AI 基礎選項（Apache 2.0 授權）。
