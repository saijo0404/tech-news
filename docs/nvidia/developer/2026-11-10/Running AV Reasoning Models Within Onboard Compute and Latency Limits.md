# Running AV Reasoning Models Within Onboard Compute and Latency Limits

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-11-10
- **原文連結**: https://developer.nvidia.com/blog/running-av-reasoning-models-within-onboard-compute-and-latency-limits/

## 核心主題
這篇文章介紹了 NVIDIA Alpamayo 2 Edge 技術，一種專為邊緣設備設計的適應性推理視覺語言行動模型，並詳細闡述了使用 AlpaJudge 評估模型的工作流。

## 關鍵重點
- **適應性推理設計**：NVIDIA Alpamayo 2 Edge 是基於 2B 參數 Nemotron 推理背骨的模型，僅在需要時生成 Chain-of-Causation 推理，顯著節省計算資源
- **性能提升**：通過閉環強化學習在 AlpaGym 中訓練，駕駛性能提升 48.9%，部分客戶在 48 小時內實現 10 Hz 實時規劃
- **推理優化**：使用 TensorRT 和 DFlash2 優化，像素到軌跡延遲僅 160-190 ms
- **評估工作流**：AlpaJudge 提供 RB/RF 兩種變體評估推理質量，通過三個步驟連接模型與改進：運行 AlpaJudge、選擇高價值樣本、使用推理分數作為獎勵
- **訓練數據選擇**：根據 AlpaJudge 分數篩選訓練數據，低分案例可能代表標籤錯誤或困難案例，高分案例表示模型已掌握，中間分數數據最具訓練價值

## 結論
NVIDIA 通過 Alpamayo 2 Edge 和 AlpaJudge 工作流，成功在邊緣設備上實現了高性能的 AV 推理模型，並通過自動化評估工作流持續優化模型性能，為未來自動駕駛系統提供了可擴展的解決方案。
---