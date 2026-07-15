# How to Run an Autoresearch Workflow with RL Agent Skills and NVIDIA NeMo

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-07-14
- **原文連結**: https://developer.nvidia.com/blog/how-to-run-an-autoresearch-workflow-with-rl-agent-skills-and-nvidia-nemo/

## 核心主題
本文介紹如何使用自主程式碼代理（Codex 搭配 GPT 5.5）結合 NVIDIA NeMo RL 與 NeMo Gym 框架，建立自動化強化學習（RL）研究工作流，實現從論文閱讀到實驗驗證的全自動化。

## 關鍵重點
- **全自動化研究工作流**：自動設置軟體堆疊、解決依賴、管理 GPU 記憶體、啟動實驗、監控執行與除錯
- **目標驅動研究**：建立基準、提出假設、執行實驗、分析指標並迭代
- **論文轉程式碼**：自動閱讀研究論文、規劃實施方案、編寫測試並啟動驗證訓練
- **實際案例成果**：Codex 成功將 Qwen3-VL-2B-Instruct 模型在視覺計數任務上的準確率從 25% 提升至 96.9%
- **人類與代理的分工**：代理負責設置、除錯、記錄和實驗循環，研究者定義目標、提供領域判斷、指導活動並決定哪些結果有意義

## 結論
自動化代理並非取代研究者，而是將重複性的設置與迭代工作交給代理，研究者仍負責設定目標、審查里程碑、指導策略與最終決策。

---