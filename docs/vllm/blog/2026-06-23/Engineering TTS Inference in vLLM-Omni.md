# Engineering TTS Inference in vLLM-Omni

- **來源**: vLLM Blog
- **發布日期**: 2026-06-23
- **原文連結**: https://vllm.ai/blog/2026-06-23-vllm-omni-tts

## 核心主題
vLLM-Omni 團隊分享優化四套文字轉語音（TTS）模型——Qwen3-TTS、VoxCPM2、Fish Speech S2 Pro、Higgs Audio V3——的推論服務經驗，揭示不同 TTS 架構的瓶頸截然不同，必須針對每種模型的特性選擇專屬優化策略。

## 關鍵重點
- **TTS 推論瓶頸不在 GPU 算力，而在服務路徑開銷**：TTS 是 Talker（延遲受限）與 Code2Wav（吞吐量受限）的多階段管線，Python 端調度、CPU→GPU 傳輸、張量分配、kernel 啟動等非運算開銷才是主要瓶頸。Qwen3-TTS 在優化前 Stage 0 GPU 利用率僅 14%，因為 GPU 大多在等 Python。
- **Qwen3-TTS：串流解耦 × 批次化 × CUDA Graph**：將 connector 串流 chunk 與 Code2Wav 解碼視窗獨立參數化，Stage 0 前處理（speaker embedding、trailing_text）全數批次化移至 GPU，並用 CUDA Graph 捕獲固定形狀解碼。結果音頻吞吐量 +61.5%（26.55→42.88 audio-s/s），P99 延遲從 17.7s 降至 9.0s（-49.4%）。
- **VoxCPM2：全前向 torch.compile × CFM 尾部批次化**：全模型 `torch.compile(fullgraph=False)` 是最大單項優化，kernel 啟動次數下降 71%。CFM/LocDiT 解碼尾部跨請求批次化讓音頻吞吐量飆升 +172.0%（12.16→33.07 audio-s/s），並將 VAE 解碼從 O(N²) 改為 O(N) 滑動視窗。
- **Fish Speech S2 Pro：專屬 attention kernel × 緩衝區重用**：通用 paged attention 在高並發下成為瓶頸，團隊實作 Fish 專屬 Triton kernel（短序列 online softmax / 長序列 split-partial-combine），並一次性分配 Fast AR 的 KV cache 重複使用，達成 23.72 audio-s/s。
- **Higgs Audio V3：多 codebook 狀態移至 GPU × 動態 batch CUDA Graph**：將複雜的多 codebook 解碼狀態機從 Python dict 移至 GPU 端批次張量，Local MLP CUDA Graph 勝過 PIECEWISE 完整圖，達成 35.26 audio-s/s（2.70× 加速）。

## 結論
vLLM-Omni 的實踐證明：TTS 推論優化沒有萬能配方。每種模型的管線結構、解碼狀態、batch 形狀和數值限制都不同，唯有辨識其獨特瓶頸——Qwen3-TTS 卡在 Python 熱路徑、VoxCPM2 卡在 CFM tiny batch、Higgs Audio V3 卡在多 codebook 狀態、Fish Speech S2 Pro 卡在通用 attention——精準選擇對應槓桿，才能發揮最大效能。

---
