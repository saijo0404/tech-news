# Post-Train NVIDIA Cosmos 3 in One Day Using Agent Skills

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-07-14
- **原文連結**: https://developer.nvidia.com/blog/post-train-nvidia-cosmos-3-in-one-day-using-agent-skills/

## 核心主題
這篇文章介紹如何結合 NVIDIA Cosmos 3 基礎模型與 NVIDIA TAO 代理技能，在一天內完成視覺語言推理模型的後訓練，將準確率從 54.41% 提升至 93.35%。

## 關鍵重點
- 使用 Low-Rank Adaptation (LoRA) 方法將零射線基準準確率從 54.41% 提升至 87.14%，再透過 TAO AutoML 優化達到 93.35%
- NVIDIA Cosmos 3 採用混合變換器 (MoT) 架構，整合多模態輸入並分離推理與生成路徑，具備卓越的視覺推理能力
- TAO 代理技能自動化處理數據處理、基準評估、LoRA 配置與超參數優化，大幅減少工程工作量，將多日任務壓縮至一天
- 生產部署透過 Cosmos 3 Reasoner NIM 簡化，直接提供 OpenAI 相容端點，無需傳統基礎設施複雜性

## 結論
結合 Cosmos 3 的結構推理能力與 TAO 自動化技能，工程師可透過兩個自然語言提示，在一天內將通用 AI 轉變為高度專門的物理 AI 模型，大幅降低後訓練門檻。

---