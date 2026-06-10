# NVIDIA Nemotron 3 Ultra 為長程代理提供更快速、更高效能的推理

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-04
- **原文連結**: https://developer.nvidia.com/blog/nvidia-nemotron-3-ultra-powers-faster-more-efficient-reasoning-for-long-running-agents/

## 核心主題
NVIDIA 發布開源模型 Nemotron 3 Ultra（550B 參數、MoE 架構，55B 活躍參數），專為長程代理（long-running agents）的複雜推理與編排任務設計，以 NVFP4 精度與多項架構創新，在維持前沿精度的同時提升 5 倍推論吞吐量，並將任務完成成本降低高達 30%。

## 關鍵重點
- **代理工作流的成本與效率痛點：單一模型難以兼顧複雜推理與高頻工具呼叫，Nemotron 3 Ultra 以 MoE 架構精準打擊「關鍵推理」節點**：長程代理需持續規劃、呼叫工具、委派子代理、驗證輸出並從錯誤恢復，導致 token 數量暴增與目標漂移；開發者應採用「模型系統」架構——前緣推理模型負責編排與複雜規劃，高效能模型負責大量執行、驗證與工具呼叫；Nemotron 3 Ultra（550B 總參數 / 55B 活躍參數）專為處理這些「困難呼叫」設計，在 Agent Productivity（PinchBench 91%）、Long-horizon Planning（EnterpriseOps-Gym 33%）、Long Context（Ruler @1M 95%）等基準上表現領先同級模型（GLM 5.1、Kimi K2.6、Qwen3.5）。
- **五大架構創新：混合 Mamba Transformer、NVFP4 精度、LatentMoE、多 token 預測與後訓練優化**：（1）後訓練（Post-training）針對代理開放式工作流優化，使用 NeMo RL 與 Gym 訓練超過百萬長程任務資料集，而非僅針對單輪聊天；（2）混合 Mamba Transformer：Mamba 層提升長上下文序列效率，Transformer 層保留精確檢索能力；（3）NVFP4 精度：單一檢查點支援 Hopper、Blackwell 與 Ampere GPU，在 Blackwell 上帶來最高 5 倍吞吐量提升；（4）LatentMoE：更有效率的專家路由，支援推理、程式碼生成、工具呼叫與領域邏輯；（5）多 token 預測（MTP）：單次前向傳播預測多個未來 token，減少生成時間；此外，引入 Multi-Teacher On-Policy Distillation（MOPD）訓練方法，超過 10 個領域專精教師模型非同步評分學生模型，實現持續協同進化。
- **完整開源生態系：訓練數據、微調腳本、安全模型與語音 ASR 一應俱全，授權改為 OpenMDW-1.1**：Nemotron 3 Ultra 全面開源——包含權重、50M 個 SFT 樣本、2M 個 RL 任務、212B 新預訓練 token（法律合成數據、Wiki 基礎數據、GitHub 程式碼）、微調腳本（LoRA SFT、全量 SFT、GRPO RL、MOPD），以及部署腳本（Dynamo Recipes）；同步發布兩款新模型：（1）Nemotron 3.5 Content Safety：4B 參數守門模型，涵蓋 23 個安全類別與 12 種語言，可作為推理時防護、LLM 安全評估裁判或後訓練資料集；（2）Nemotron 3.5 ASR：支援 40+ 語言的流語音辨識模型，延遲低於 100 毫秒，已應用於 Microsoft GitHub Copilot CLI（超過 2,000 萬開發者使用）；授權從傳統模式改為 Linux Foundation 的 OpenMDW-1.1 許可，涵蓋模型架構、參數、文件與軟體；生態系夥伴涵蓋 SGLang、vLLM、TRT-LLM、AWS SageMaker、Google Cloud、Microsoft Foundry、CoreWeave 等，並提供 Hermes Agent、OpenHands、CrewAI 等代理框架的整合腳本。

## 結論
Nemotron 3 Ultra 代表 NVIDIA 從「通用語言模型」轉向「代理原生模型」的關鍵一步——它不再只是單輪對話的聊天機器人，而是專為長程、多步驟、高成本代理工作流設計的推理引擎；透過 MoE 架構（550B/55B）精準聚焦資源於「關鍵推理節點」、NVFP4 精度實現跨世代 GPU 相容與 5 倍吞吐量、MOPD 多教師協同訓練持續進化能力，Nemotron 3 Ultra 在維持前沿精度的同時將代理任務完成成本降低 30%；加上全面開源（權重、數據、訓練腳本）、配套安全模型（Content Safety）與多語言語音 ASR、以及 OpenMDW-1.1 清晰授權，NVIDIA 正在建構一個從「模型訓練」到「代理部署」的完整開源生態系；對於開發者而言，這意味著可以用同一個模型替代過去需要多個模型才能完成的代理編排任務，同時以更低成本、更高效率運行於任何 NVIDIA GPU 架構之上。
