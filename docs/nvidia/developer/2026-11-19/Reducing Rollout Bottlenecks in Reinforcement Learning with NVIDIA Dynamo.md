# Reducing Rollout Bottlenecks in Reinforcement Learning with NVIDIA Dynamo

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-11-19
- **原文連結**: https://developer.nvidia.com/blog/reducing-rollout-bottlenecks-in-reinforcement-learning-with-nvidia-dynamo/

## 核心主題
NVIDIA Dynamo 提供一個服務層，協調強化學習訓練中的分布式 rollout 生成，透過 KV-aware routing、ModelExpress 權重分佈和 Recovery 機制解決 rollout 瓶頸問題。

## 關鍵重點
- **KV-aware routing**：平衡 KV 快取重使用和 worker 負載，減少重複提示計算和 rollout 延遲
- **ModelExpress**：加速權重分佈，透過轉移壓縮的 delta 更新和重用已駐留在 GPU 記憶體中的權重，避免從遠端儲存載入完整檢查點
- **Recovery 機制**：檢測 worker 失敗，將請求重導向健康容量，並讓替換 worker 使用檢查點和 delta 載入跟進訓練進度

## 結論
Dynamo 幫助團隊在固定計算預算內完成更多強化學習迭代，透過優化 rollout 生成、權重分佈和 worker 恢復，加速訓練進度並提升 GPU 資源利用率。

---

已將摘要成功儲存至指定檔案路徑。