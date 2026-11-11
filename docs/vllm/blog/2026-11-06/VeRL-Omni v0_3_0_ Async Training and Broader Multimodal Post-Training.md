# VeRL-Omni v0.3.0: Async Training and Broader Multimodal Post-Training

- **來源**: vLLM Blog
- **發布日期**: 2026-11-06
- **原文連結**: https://vllm.ai/blog/2026-11-06-verl-omni-v0-3-0

## 核心主題
VeRL-Omni v0.3.0 擴展了單一統一堆疊中可訓練的 RL 工作負載，帶來異步執行、V1 訓練器預設和更廣泛的多模態後訓練覆蓋。

## 關鍵重點
- **異步和解耦的 RL 執行**：支援完全異步 rollout，將 actor 和 rollout engine 置於獨立 GPU 池，透過 replay buffer 連接生成與訓練，並提供可配置的同步間隔。
- **共享的 V1 訓練基礎設施**：V1 訓練器（基於 TransferQueue 和 ReplayBuffer）成為預設，擴展至擴散模型，強化 rollout 與訓練交接，並引入命名媒體藝術品以明確處理圖片、視頻、音頻和潛在輸出。
- **MiniMax H3 音頻視頻後訓練**：支援 FlowGRPO 和 DiffusionNFT，提供 T2VA（文本到音頻視頻）和 FL2VA（首幀圖像到音頻視頻）完整訓練流程，使用 CLAP 和 ImageBind 作為獎勵指標。
- **MiniCPM-o 4.5 GSPO，同步與異步比較**：Group Sequence Policy Optimization (GSPO) 應用於音頻視覺問答（AVQA），比較 colocated sync 與 separate-async 執行模式，在長回應場景下 separate-async 可達 6.7% 更快。
- **模型和演算法擴展**：新增 MiniMax H3、BOOGU-Image、MiniCPM-o 4.5 Thinker、Qwen3-TTS、FLUX.1-dev DanceGRPO、LTX-2.3、Qwen3-Omni 等多個模型和演算法支援。

## 結論
此發布為多模態 RL 訓練提供了更靈活的工具，讓使用者可以根據工作負載選擇合適的執行模式。關鍵在於衡量 GPU 分佈、生成長度與訓練器關鍵路徑，以決定 colocated sync 或 separate-async 哪個更適合特定場景。

---

最後，完整的摘要已成功儲存至指定檔案路徑。
