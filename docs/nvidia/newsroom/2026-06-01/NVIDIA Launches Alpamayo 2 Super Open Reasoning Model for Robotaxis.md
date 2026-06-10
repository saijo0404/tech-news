# NVIDIA 推出 Alpamayo 2 Super 開源推理模型，打造 Robotaxi 新世代

- **來源**: NVIDIA Newsroom
- **發布日期**: 2026-05-31
- **原文連結**: https://nvidianews.nvidia.com/news/nvidia-alpamayo-2-super-robotaxis

## 核心主題
NVIDIA 發布 320 億參數的 Alpamayo 2 Super 開源推理 VLA 模型，結合 AlpaGym 閉環訓練框架、OmniDreams 世界模型與物理 AI 代理技能，建構從真實資料擷取、閉環訓練到車載部署的完整自動駕駛開發管道。

## 關鍵重點
- **32B 參數推理模型具備人類級感知能力**：Alpamayo 2 Super 以 Cosmos 基礎模型為基底，參數量從 10B 擴展至 32B，支援 360 度全景感知、Meta-Actions 高階駕駛決策輸出、推理自動標註（縮短標註週期從數月到數天）及改進的因果鏈（CoC）追蹤，可作為教師模型蒸餾為部署於 DRIVE AGX Thor 的輕量模型。
- **AlpaGym 閉環強化學習與 OmniDreams 場景生成**：AlpaGym 將模型在 AlpaSim 模擬器中的連續決策循環與環境反饋直接連結，揭示靜態資料無法捕捉的連鎖錯誤與長尾失敗案例；OmniDreams 則能大規模生成照片級真實的稀有與長尾駕駛場景。
- **物理 AI 代理技能加速開發效能**：NVIDIA 提供基於 Omniverse NuRec 的神經重建技能、OmniDreams 場景生成技能與 AlpaGym 閉環 RL 技能，讓開發者與程式碼代理能自動化完成模擬、資料生成與閉環訓練，自 Alpamayo 推出以來總下載量已近 40 萬次。

## 結論
Alpamayo 2 Super 讓自動駕駛系統從「會開」進化到「會推理」，結合 NVIDIA 完整的開源模型、模擬器、真實數據與代理技能生態系，為全球 Robotaxi 產業提供安全、可解釋、可擴展的 Level 4 開發基礎，Alpamayo 2 Super 預計於今夏在 GitHub 與 Hugging Face 開放。
