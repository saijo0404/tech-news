# Adapt Human Motion for Robots with NVIDIA SOMA Retargeter

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-11-13
- **原文連結**: https://developer.nvidia.com/blog/adapt-human-motion-for-robots-with-nvidia-soma-retargeter/

## 核心主題
介紹 NVIDIA SOMA Retargeter 工具，用於將人類動作適配到不同人形機器人上。

## 關鍵重點
- 使用共享的 SOMA 骨架表示法，將人類動作數據適配到人形機器人的比例和關節結構上
- 提供從動作捕捉數據集（如 BONES-SEED）、視頻重建（如 GEM-X）或生成模型（如 Kimodo 和 ARDY）等多種來源的人類動作
- 支援五種人形機器人（Unitree G1、Unitree H2、Booster T1、AgiBot X2 Ultra、AgiBot A3T3）的參考配置和適配結果
- 包含 Robot Configurator 和 IK 權重優化器等工具，幫助調整參考姿勢、映射骨架和優化逆運動學優先級
- 輸出 CSV 檔案並轉換為運動庫格式，用於 SONIC 和 ProtoMotions 等政策訓練工作流

## 結論
SOMA Retargeter 為開發者提供了完整的工具鏈，從人類動作適配到機器人控制策略訓練，並支援批量處理和模擬評估。
---