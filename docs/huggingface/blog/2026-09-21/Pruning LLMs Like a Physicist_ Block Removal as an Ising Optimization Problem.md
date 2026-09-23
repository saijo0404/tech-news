# Pruning LLMs Like a Physicist: Block Removal as an Ising Optimization Problem

- **來源**: Hugging Face Blog
- **發布日期**: 2026-09-21
- **原文連結**: https://huggingface.co/blog/MultiverseComputingCAI/pruning-llms-like-a-physicist-block-removal-as-an

## 核心主題
這篇文章提出將大型語言模型的區塊移除問題建模為物理學中的 Ising 優化問題，通過考慮區塊間的相互作用來優化剪枝策略。

## 關鍵重點
- 傳統方法將每個區塊視為獨立，忽略了區塊間的相互依賴關係，而本文提出將剪枝問題轉化為能量最小化問題
- 通過二階泰勒展開和 Hessian 矩陣計算，將剪枝問題轉化為能量最小化問題，能量是下游品質的強有力代理
- 在 Llama-3.3-70B-Instruct 模型上，50% 壓縮率下比競爭方法多獲得近 23 個百分點
- 最佳剪枝配置往往不是能量最低態，而是低能激發態，這挑戰了傳統剪枝方法假設

## 結論
將剪枝問題建模為 Ising 優化問題，並使用量子啟發式求解器，在深度壓縮下顯著提升了模型性能，特別適合處理現代異構架構。
---
