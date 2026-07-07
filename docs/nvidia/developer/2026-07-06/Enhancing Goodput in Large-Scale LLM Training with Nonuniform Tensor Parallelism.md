# Enhancing Goodput in Large-Scale LLM Training with Nonuniform Tensor Parallelism

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-07-06
- **原文連結**: https://developer.nvidia.com/blog/enhancing-goodput-in-large-scale-llm-training-with-nonuniform-tensor-parallelism/

## 核心主題
Nonuniform Tensor Parallelism (NTP) 技術透過動態調整張量並行度，使大規模 LLM 訓練工作能夠適應 GPU 可用性波動，確保持續的 Goodput 並最小化停滯與吞吐量損失。

## 關鍵重點
- **動態 TP 度適應**：當 TP 群組中出現 GPU 故障時，系統自動調整張量並行度以利用剩餘功能 GPU，避免訓練中斷
- **動態電源提升**：透過增加電源供應，提升剩餘 GPU 的時鐘頻率與吞吐量，補償因 TP 度減少帶來的性能損失
- **高效重疊重新分佈**：採用與後向計算和參數同步階段重疊的重新分佈技術，引入的過載小於 1%

## 結論
NTP 展示了硬體與軟體協同設計的重要性，透過將韌性直接整合到並行策略中，為下一代 AI 系統帶來更高的性能、效率與韌性。

---

*AI-generated content may summarize information incompletely. Verify important information.*
