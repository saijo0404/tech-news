# ALTK-Evolve: How learned memory tops the τ²-bench leaderboard on customer service tasks without a frontier model

- **來源**: Hugging Face Blog
- **發布日期**: 2026-10-20
- **原文連結**: https://huggingface.co/blog/ibm-research/altk-evolve-bc

## 核心主題
IBM Research 開發的 ALTK-Evolve 系統透過學習記憶機制，讓基於 GPT-4.1 的基本客戶服務代理在 τ²-bench 排行榜上超越所有競爭對手，且無需更新模型權重。

## 關鍵重點
- **學習記憶機制**：系統使用同一個 GPT-4.1 模型，從訓練任務中提取成功與失敗經驗，轉化為行為規則（如驗證客戶身份、確認交易變更、處理退貨等），並追加到系統提示中。
- **雙領域表現提升**：在零售領域，使用完整指導規則（lossless 配置）可將 Pass^4 從 57.5% 提升至 67.5%；在航空領域，高支持度的核心規則（sup3 配置）即可達到 45% Pass^4。
- **成本效益優化**：性能提升來自更精確的提示而非更長的對話，實際對話輪數反而減少，且輸入成本可透過提示緩存大部分回收。
- **適用性驗證**：該方法不僅適用於 GPT-4.1，對 frontier 模型（如 GPT-5.5）同樣有效，且可靠性提升幅度更大（Pass^4 從 55% 提升至 70%）。

## 結論
ALTK-Evolve 證明透過學習記憶而非模型重訓練，即可顯著提升客戶服務代理的準確性與可靠性，同時保持成本效益與低延遲，為可部署的 AI 系統提供了新的優化路徑。
---
