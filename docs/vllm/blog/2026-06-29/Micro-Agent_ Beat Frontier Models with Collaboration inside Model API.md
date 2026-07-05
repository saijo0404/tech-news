# Micro-Agent: Beat Frontier Models with Collaboration inside Model API

- **來源**: vLLM Blog
- **發布日期**: 2026-06-29
- **原文連結**: https://vllm.ai/blog/2026-06-29-micro-agent-frontier-models

## 核心主題
vLLM Semantic Router 提出「微代理（Micro-Agent）」概念，將模型協作（collaboration）內建於服務層而非應用層，透過任務適配的合作模式（如 Confidence、Ratings、ReMoM、Fusion、Workflows）在單一 API 呼叫下超越單一 frontier 模型的表現。

## 關鍵重點
- **路由從選模型到建能力**：傳統路由僅負責將請求分發到合適模型，而 vLLM Semantic Router 讓路由成為「能力建構平面」，在服務層內執行有預算、有頂限的協作邏輯，讓單一 API 呼叫感覺像單一模型。
- **五種協作模式**：
  - **Confidence**：依置信度逐步升級，僅在低分時才調用更貴模型，節省成本。
  - **Ratings**：並行呼叫多個候選模型，依評分加權聚合，適合 A/B 測試與 ensemble 策略。
  - **ReMoM**：重複混合模型推理，等待足夠成功的回應後由合成模型合併證據，適合高變異任務。
  - **Fusion**：將獨立模型的差異轉化為證據，由裁判模型從分歧中合成最終答案，適合多解任務。
  - **Workflows**：微代理工作流運行，支援靜態或動態規劃者，執行有預算限制的步驟，適合 SWE 風格任務。
- **任務形狀決定最佳模式**：不同任務（如 GPQA-Diamond、LiveCodeBench、Humanity's Last Exam）需要不同合作模式，vLLM Semantic Router 透過路由訊號自動選擇最適合的「食譜（recipe）」，而非固定使用單一算法。
- **超越單一模型**：評估顯示，vLLM Semantic Router 在 LiveCodeBench 上達 92.6 分，GPQA-Diamond 達 96.0 分，Humanity's Last Exam 達 50.0 分，超越或匹敵單一 frontier 模型，同時保持單一 API 介面。
- **開放與封閉模型共存**：系統可混合使用開放與封閉模型，在需要高風險判斷、修復或合成時優先使用封閉模型，在一般任務使用開放模型，透過服務層抽象統一管理。

## 結論
vLLM Semantic Router 將微代理從應用層邏輯移至服務層基礎設施，讓路由不僅能選模型，更能「建構能力」。透過任務適配的合作模式與嚴格預算控制，微代理在保持單一 API 介面下，能超越單一 frontier 模型的表現。這標誌著 AI 服務從「被動傳遞」轉向「主動協作」的新階段，未來競爭將不僅在於模型本身，更在於路由的協作策略與可觀測性。
---
