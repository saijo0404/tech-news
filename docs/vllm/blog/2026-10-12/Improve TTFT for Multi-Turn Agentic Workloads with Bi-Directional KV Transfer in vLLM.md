# Improve TTFT for Multi-Turn Agentic Workloads with Bi-Directional KV Transfer in vLLM

- **來源**: vLLM
- **發布日期**: 2026-10-12
- **原文連結**: https://vllm.ai/blog/2026-10-12-bidirectional-kvxfer-multiturn-agentic-workload

## 核心主題
vLLM 推出雙向 KV 轉移技術，用於改善多輪代理工作負載的首次 token 時間 (TTFT)，通過允許 decode 節點保留已生成的 KV 並在後續輪次中返回給 prefill 節點，避免重複計算。

## 關鍵重點
- 傳統 P-D 分離架構僅支持單向 KV 轉移（prefill→decode），導致 decode 節點產生的 KV 無法被下一個 prefill 節點重用，造成重複計算，使 TTFT 隨對話輪次增加而顯著上升。
- 雙向 KV 轉移機制允許 decode 節點保留已生成的 KV，並在後續輪次中返回給 prefill 節點，避免重複計算。由 KV-cache-aware router 協調 KV 元數據傳輸。
- 在 Amazon EC2 P5en 實例測試中：Qwen3-32B 的 TTFT 最多降低 1.6 倍，GLM-5-FP8 的 TTFT 最多降低 3.3 倍。
- 實施方式：使用 vLLM v0.21.0 或更高版本，啟用 bidirectional_kv_xfer，並配置 KV-cache-aware router。可透過調整 decoder_kv_blocks_ttl（預設 480 秒）與 kv_recompute_threshold（預設 64 tokens）來平衡 KV 重用與記憶體使用。

## 結論
雙向 KV 轉移技術顯著改善了多輪代理工作負載的首次 token 時間，特別是在長上下文場景下表現突出，有效降低因重複計算帶來的延遲，提升應用響應速度。
---
