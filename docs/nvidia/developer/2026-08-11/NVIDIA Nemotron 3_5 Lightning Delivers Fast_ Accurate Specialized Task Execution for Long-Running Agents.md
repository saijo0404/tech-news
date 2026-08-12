# NVIDIA Nemotron 3.5 Lightning Delivers Fast, Accurate Specialized Task Execution for Long-Running Agents

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-08-11
- **原文連結**: https://developer.nvidia.com/blog/nvidia-nemotron-3-5-lightning-delivers-fast-accurate-specialized-task-execution-for-long-running-agents/

## 核心主題
NVIDIA Nemotron 3.5 Lightning 是一款專為長期運行 AI 代理設計的 30B 參數開源混合專家（MoE）模型，以 3B 活躍參數實現高吞吐量、低延遲的執行效率。

## 關鍵重點
- **MoE 架構優勢**: 採用混合專家架構，僅激活 3B 參數即可實現大模型能力，大幅降低計算成本並提升執行速度。
- **4 倍輸出速度**: 相比同級模型提供最高 4 倍的輸出速度，在 PinchBench 測試中比 Qwen3.6 35B 快 30%。
- **專用推理優化**: 支援 speculative decoding（推測解碼）、DFlash 和 DSpark 草稿模型，並提供 NVFP4 和 BF16 量化檢查點。
- **開源生態系統**: 提供寬鬆授權、權重、數據和訓練配方，可透過 LoRA、全量 SFT 或強化學習進行自訂。
- **模型路由整合**: 透過 NVIDIA NeMo Switchyard 實現智能模型路由，將高頻執行任務分配給 Nemotron 3.5 Lightning，複雜規劃任務交由 frontier 模型處理。

## 結論
NVIDIA Nemotron 3.5 Lightning 透過開源架構與專用優化技術，成功在準確性與速度之間取得最佳平衡，為長期運行的 AI 代理提供高效、可自訂的執行層解決方案，並可部署於從桌面到數據中心的各種硬體環境。
---