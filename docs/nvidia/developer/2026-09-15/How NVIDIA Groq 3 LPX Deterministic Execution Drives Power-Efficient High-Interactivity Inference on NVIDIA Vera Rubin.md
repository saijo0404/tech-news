# How NVIDIA Groq 3 LPX Deterministic Execution Drives Power-Efficient High-Interactivity Inference on NVIDIA Vera Rubin

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-09-15
- **原文連結**: https://developer.nvidia.com/blog/how-nvidia-groq-3-lpx-deterministic-execution-drives-power-efficient-high-interactivity-inference-on-nvidia-vera-rubin/

## 核心主題
NVIDIA Groq 3 LPX 透過確定性執行模型，結合 Vera Rubin NVL72 平台，實現高互動性推理時的高效能與低功耗。

## 關鍵重點
- Groq 3 LPX 採用確定性執行模型，可精確到時鐘週期地排程運算與資料移動，支援 256 個 LPU 晶片
- 透過 Preemptive Power (PEP) 和 Clock Period Synthesis (CPS) 技術，減少電壓波動超過 60%，降低電壓守衛帶寬
- 與 Vera Rubin NVL72 搭配，對 2T+ 參數模型實現每兆瓦 35 倍以上的吞吐量提升，支援長上下文與高互動性推理

## 結論
Groq 3 LPX 的確定性執行模型透過可預測的電流需求曲線，大幅降低電壓守衛帶寬，使 AI 工廠能在相同電力預算下獲得更高吞吐量，是 NVIDIA Vera Rubin 平台實現效能每瓦特最大化的關鍵創新。
---