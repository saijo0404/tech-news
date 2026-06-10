# 使用 NVIDIA Cosmos 3 開發實體 AI 推理、世界與動作模型

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-05-31
- **原文連結**: https://developer.nvidia.com/blog/develop-physical-ai-reasoning-world-and-action-models-with-nvidia-cosmos-3/

## 核心主題
NVIDIA 全面開放 Cosmos 3 模型、訓練腳本、部署工具與數據集，透過雙塔混合 Transformer 架構（推理塔＋生成塔）統一物理推理、世界生成與動作生成，讓開發者能為機器人、自動駕駛與智慧空間開發實體 AI 模型。

## 關鍵重點
- **雙塔混合 Transformer 架構**：推理塔（Reasoner）以自回歸 VLM 解釋多模態觀察並理解物理情境，生成塔（Generator）以擴散流程生成物理感知的影片與動作輸出，單一模型即可完成推理與生成任務，免除多模型協調的複雜度。
- **雙版本模型與六大開放數據集**：Cosmos 3 Nano（8B 參數）適合工作站級即時推理，Cosmos 3 Super（32B 參數）適合資料中心高品質生成；同步開放機器人、物理模擬、空間推理、數位人類、自動駕駛與倉庫操作的六大合成數據集。
- **完整訓練與部署工具鏈**：提供監督式微調（SFT）與動作後訓練腳本，支援未來狀態預測、逆動力學與策略生成；NIM 微服務支援 BF16/FP8/NVFP4 量化與 Efficient Video Sampling 加速推理，NVIDIA Cosmos 人類評估（HUE）框架則以原子二元驗證取代主觀評分。

## 結論
Cosmos 3 以 OpenMDW 1.1 授權全面開放，讓開發者能從 Hugging Face 下載權重、透過 GitHub 存取訓練腳本、以 NIM 微服務部署推理，建構從數據生成、後訓練到生產部署的實體 AI 完整開發體驗。
