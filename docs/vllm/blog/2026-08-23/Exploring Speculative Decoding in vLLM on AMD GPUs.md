# Exploring Speculative Decoding in vLLM on AMD GPUs

- **來源**: vLLM Blog
- **發布日期**: 2026-08-23
- **原文連結**: https://vllm.ai/blog/2026-08-23-speculative-decoding-amd-gpus

## 核心主題
本文探討 vLLM 在 AMD GPU 平台上的推測解碼（speculative decoding）技術，比較五種不同的 draft 方法（Native MTP、Gemma 4 MTP、EAGLE-3、DFlash、DSpark）的性能表現與最佳實踐。

## 關鍵重點
- **推測解碼原理**：透過輕量 draft 組件預測多個候選 token，再由目標模型一次性驗證，可減少目標模型的解碼次數，提升吞吐量。
- **五種 Draft 方法比較**：
  - **Native MTP**：內建於目標模型架構，序列式生成，準確性最高但速度較慢
  - **Gemma 4 MTP**：獨立 checkpoint 搭配特定目標模型，共享 KV cache，序列式生成
  - **EAGLE-3**：專用 draft 網路，序列式 autoregressive 生成，平衡速度與準確性
  - **DFlash**：專用 draft 網路，平行預測所有位置，速度提升顯著（最高 2.87×）但準確性略降
  - **DSpark**：DFlash + 輕量 Markov head，中等速度與準確性平衡
- **性能測量結果**：
  - 最高 Throughput 提升：DFlash (MATH500) 達 2.87×，Gemma 4 MTP (GSM8K) 達 2.74×
  - 最佳 Proposal Length：依 workload 變化，通常 N=4~7，部分方法 N=7 表現最佳
  - Acceptance Rate：取決於任務結構與可預測性，N=1 時 AR 最高 (96-97%)
- **模型表現差異**：
  - **Gemma 4 系列**：MTP 推理方式表現最穩定（Gemma 4-26B tok/s 達 6,161，AR 94%）
  - **Qwen3-8B**：DSpark 推理方式展現最佳速度（tok/s 達 6,032，AR 95%）
  - **Qwen 系列大模型**：122B 模型性能最高，但 DFlash 推理方式會導致性能下降
- **實驗環境**：測試於 AMD Instinct MI300X 與 MI355X GPU，使用 ROCm 平台，涵蓋 Gemma、Qwen、Kimi 等多個模型系列
- **最佳實踐**：
  1. 從 checkpoint 推薦配置開始
  2. 使用代表性 workload 進行端對端測量
  3. 根據吞吐量、接受率等指標而非僅接受率選擇配置
  4. 訓練 speculator 時需準備代表性提示並收集目標模型 hidden states

## 結論
推測解碼技術能顯著提升 LLM 推理速度，但效能表現受 drafting 方法、模型家族、draft checkpoint、workload 特性及接受行為等多重因素影響。使用者需根據準確性要求與速度需求進行權衡：追求平衡可選擇 EAGLE-3，追求速度則 DFlash 表現最佳，但需監控準確率下降風險。未來方向包括擴展至非學習方法（如 n-gram speculation）及深入分析 draft generation 與 verification 行為。

---