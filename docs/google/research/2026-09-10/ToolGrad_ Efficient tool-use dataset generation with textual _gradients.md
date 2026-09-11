# ToolGrad: Efficient tool-use dataset generation with textual "gradients"

- **來源**: Google Research Blog
- **發布日期**: 2026-09-10
- **原文連結**: https://research.google/blog/toolgrad-efficient-tool-use-dataset-generation-with-textual-gradients/

## 核心主題
ToolGrad 是一種數據生成框架，顛覆傳統範式，先生成工具使用答案再產生用戶查詢，使 LLM 能更有效率地學習工具使用。

## 關鍵重點
- **答案優先方法**：與傳統「查詢優先」方法不同，ToolGrad 先生成正確的工具使用鏈，再標註對應用戶提示，大幅降低標註成本。
- **文本梯度優化**：利用文本梯度 (textual gradients) 迭代構建複雜 API 工作流，通過 API 提案器、執行器、選擇器和更新器四個核心模組逐步優化。
- **高成功率**：在 ToolBench 數據集上達到 99.8% 的通過率，遠超傳統 DFS 方法的低成功率。
- **性能優異**：訓練後的 ToolGrad-12B 模型在 Berkeley Function Calling Leaderboard 上得分 83.1，與 Gemini 2.5 Pro (83.2) 等私有模型相當，甚至超越部分開源模型。
- **學生超越教師**：用 Gemini 2.5 Flash Lite 生成的數據訓練 Gemma-3-12B，表現優於原始教師模型，展現自進化的潛力。

## 結論
ToolGrad 證明透過「答案優先」的框架設計，能以更高效率和可靠性生成高品質工具使用數據集，解決了傳統方法在成本和可擴展性上的瓶頸，為訓練高效且經濟的數字智能體奠定基礎。

---