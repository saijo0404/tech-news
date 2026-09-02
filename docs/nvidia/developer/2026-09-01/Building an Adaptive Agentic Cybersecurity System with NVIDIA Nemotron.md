# Building an Adaptive Agentic Cybersecurity System with NVIDIA Nemotron

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-09-01
- **原文連結**: https://developer.nvidia.com/blog/building-an-adaptive-agentic-cybersecurity-system-with-nvidia-nemotron/

## 核心主題
NVIDIA 與 CrowdStrike 合作，利用 Nemotron 開源模型建立了一個驗證優先的攻防代理系統，在模擬 NVIDIA 加速計算基礎設施的隔離環境中實現了機器速度的連續閉環。

## 關鍵重點
- 防禦 harness 整合了六項機制（知識庫、電訊 grounding、專用檢測撰寫、linting、檢測重放、獨立審查）以產生接地、可測試的檢測
- Nemotron 3 Ultra 負責防禦協調，經過後訓練的 Nemotron 3 Super 作為有界專家進行檢測生成與修復
- 使用 NVIDIA NeMo Gym 和 NeMo RL 進行強化學習，基於可驗證獎勵進行訓練
- 回測顯示優化開源模型管道檢測率提升 2.5 倍（41.9%），遠超僅使用 Nemotron 3 Ultra 的預設 harness
- 實戰測試中 45% 開源模型檢測泛化（vs 前鋒系統的 29%），3 個開源檢測成為金級檢測並覆蓋所有 8 次攻擊

## 結論
開源模型驅動的代理系統在泛化能力和檢測質量上優於前鋒系統，為安全團隊提供了更具成本效益（99% 更低成本）且準確性更高的解決方案，並展示了將攻防活動整合為連續學習閉環的可行性。
---
