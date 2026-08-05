# Generate Trajectories, Reasoning Traces, and Auto-Labels with NVIDIA Alpamayo 2 Super

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-08-04
- **原文連結**: https://developer.nvidia.com/blog/generate-trajectories-reasoning-traces-and-auto-labels-with-nvidia-alpamayo-2-super/

## 核心主題
NVIDIA Alpamayo 2 Super 是一款結合周視感知、推理與規劃能力的開源 VLA 模型，提供多任務輸出與自動標記功能，可加速自動駕駛開發流程。

## 關鍵重點
- **340 億參數開源模型**：整合 32B Cosmos 3 Super Reasoner 與 2B Action Expert，支援最多 7 個攝影機的 360 度感知
- **多任務能力**：提供未來軌跡預測、因果鏈推理、高階元動作預測、VQA 與自動標記功能
- **優異性能表現**：軌跡預測 minADE_6: 0.911m (SOTA)、AV 推理 0.433、LingoQA 79.2 (領先同級模型)
- **自動標記效率**：可將標註週期從數月壓縮至數天，支援衝突行為 (CoC) 自動標記
- **商用授權**：OpenMDW-1.1 許可，可商用分發，模型權重提供於 Hugging Face
- **可部署性**：可精簡為可在 NVIDIA DRIVE AGX Thor 運行的緊湊模型

## 結論
NVIDIA Alpamayo 2 Super 作為開放模型工作流，提供從感知到推理、規劃到自動標記的全流程能力，可作為離線政策教師、評估批評者或數據引擎，顯著提升自動駕駛開發與評估效率。模型已在 GitHub 提供推理筆記本，方便開發者快速上手。