# The Definitive Fine-Tuning Guide for 3D Generation Models

- **來源**: Hugging Face Blog
- **發布日期**: 2026-11-12
- **原文連結**: https://huggingface.co/blog/3d-lora-finetuning

## 核心主題
這篇文章介紹了如何使用 LoRA 技術對 TRELLIS.2 3D 生成模型進行微調，以生成特定類別的 3D 物件（如鞋類），並提供了完整的訓練流程與評估結果。

## 關鍵重點
- 使用 LoRA 技術僅訓練少量 adapter 參數，降低記憶體需求
- 針對鞋子生成任務，在稀疏結構流和形狀流模型組件上進行微調
- 訓練結果顯示 F-score 從 0.276 提升至 0.803，Chamfer distance 從 0.174 降至 0.033
- 微調後的模型在鞋底細節生成上表現顯著提升

## 結論
LoRA 微調方法為 3D 生成模型提供了高效且精準的訓練方案，特別適合小數據集場景，可避免全量微調的高成本與災難性遺忘問題。

---

訓練流程包括：
1. 數據準備：將 GLB/OBJ 轉換為 TRELLIS.2 潛變表示
2. 預處理：使用 Blender 渲染 16 個視角
3. 訓練：在 a100-large 上運行訓練容器，訓練約 930 萬 adapter 參數

評估指標改善：
- F-score: 0.276 → 0.803
- Chamfer distance: 0.174 → 0.033
- Normal consistency: 0.530 → 0.804

此方法建議未來可應用到其他 3D 生成模型（如 Pixal3D、UniLat3D 等）。