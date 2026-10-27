# Serving DeepSeek-V4.1-Flash at Scale: vLLM Matches DeepInfer and Scales to GB300 NVL72

- **來源**: vLLM Blog
- **發布日期**: 2026-10-23
- **原文連結**: https://vllm.ai/blog/2026-10-23-deepseek-v41-flash-pd-wide-ep

## 核心主題
vLLM 在 NVIDIA GB300 NVL72 機架上使用 P/D 分散與 Wide-EP 技術，成功服務 DeepSeek-V4.1-Flash 模型，性能達到 DeepInfer 引擎的 95% 以上，證明通用引擎可匹敵模型專用引擎。

## 關鍵重點
- **單 GPU 吞吐量達 954K tokens/s**：在 SemiAnalysis AgentX 上，vLLM 以 P90 196 tokens/s 的用戶性能，是單機結果的 7.9 倍
- **單用戶專用解碼路徑**：可達 826 tokens/s，大幅降低延遲
- **與 DeepInfer 性能接近**：vLLM 解碼吞吐量在批次大小 8-256 範圍內與 DeepInfer 差異僅 6% 以內，prefill 追蹤 DeepInfer 發布曲線
- **關鍵優化措施**：
  - 小 DEP 實例（DEP2）用於 prefill，減少 DP 不平衡影響
  - Wide-EP 解碼有效降低 MoE 權重讀取成本
  - EPLB 專家平衡提升專家分佈均衡度
  - 擴展 SWA 有界重播至 Layer 20、使用 2MB 頁表、DeepSelect top-k 索引
  - 優化 CPU 超時：NIXL 推送、遞減所有歸約、 admission 限制
- **架構優勢**：DeepSeek-V4.1-Flash 具有小 KV Cache（890 bytes/token）、輕量注意力機制，解碼延遲對上下文長度不敏感

## 結論
vLLM 通過深入理解模型架構（如 Small KV cache、MoE-bound 解碼）並針對性優化現有組件，成功在 GB300 NVL72 規模下達到與 DeepInfer 相當的性能，同時大幅降低延遲與成本（$38.96/GPU-hour）。這證明通用推理引擎只要充分理解模型特性，就能在特定模型上達到專用引擎的水平。

---