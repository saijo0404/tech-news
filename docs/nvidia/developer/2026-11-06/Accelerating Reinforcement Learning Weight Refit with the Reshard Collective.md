# Accelerating Reinforcement Learning Weight Refit with the Reshard Collective

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-11-06
- **原文連結**: https://developer.nvidia.com/blog/accelerating-reinforcement-learning-weight-refit-with-the-reshard-collective/

## 核心主題
這篇文章介紹了 Reshard collective 如何加速強化學習中的權重重新分配（refit）過程，通過將權重轉移重新定義為 DTensor 到 DTensor 的轉移，大幅減少通信數據量並提升效率。

## 關鍵重點
- 傳統 gather-and-broadcast 方法效率低，通信載荷大（約 10 TB），每個權重參數都需要先匯集再廣播，造成冗餘傳輸
- Reshard collective 將 refit 重新定義為 DTensor-to-DTensor 轉移，只傳輸理論最小數據，直接從源片段傳輸到目標片段
- NCCL M2N Reshard 實現了此 collective，通過計算片段交集和分組 NVLink 域副本來消除冗餘網絡傳輸，最大化網絡頻寬
- 在 NeMo RL 測試中，Reshard refit 比傳統方法快 2.7 到 5.7 倍，適用於 Qwen 3 235B 和 DeepSeek v3 671B 等大型模型
- NeMo RL 採用混合方法，對佔比最大的前饋投影權重使用 Reshard，其他小權重使用傳統方法以維持功能覆蓋

## 結論
Reshard collective 為大型模型強化學習訓練提供了更高效的權重轉移解決方案，顯著降低了通信負載並提升了訓練速度，特別適合處理超大型語言模型。

---