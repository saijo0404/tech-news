# MiniMax M3 在 vLLM 中的首日支援：為 1M Token 多模態推理提供高效能部署

- **來源**: vLLM Blog
- **發布日期**: 2026-06-12
- **原文連結**: https://vllm.ai/blog/2026-06-12-minimax-m3-vllm

## 核心主題
vLLM 宣布為 MiniMax M3 模型家族提供首日（Day-0）支援，涵蓋 BF16 與 MXFP8 權重，完整支援百萬 Token 上下文、MiniMax 稀疏注意力（MSA）、多模態推理、工具呼叫與 EAGLE3 假設解碼，讓開發者能直接部署具備生產級效能的 M3 模型服務。

## 關鍵重點
- **MiniMax 稀疏注意力（MSA）架構**：MSA 將固定 128 Token 的 KV Block 進行評分與篩選，僅對選定區塊執行 GQA 注意力運算，在維持百萬 Token 上下文能力的同時大幅降低計算開銷，並透過 KV-Block-Major Prefill 與最佳化的 Decode Indexer 核心提升吞吐量。
- **首日多項關鍵功能**：內建 minimax_m3 工具與推理輸出解析器、支援 Thinking Mode（可控制思考行為）、整合 MXFP8 MoE 後端（DeepGEMM on Blackwell / Marlin on Hopper）、支援 EAGLE3 假設解碼（搭配 Inferact 發布的 Draft 模型），以及完整的 NIM 與 NeMo RL 強化學習後訓練路徑。
- **跨硬體平台部署與效能優化**：支援 NVIDIA（H200、GB200、B300）與 AMD（MI300、MI350）加速器，提供 Block-Size 128 對齊、Chunked Prefill、Prefix Caching 等生產級部署建議；驗證數據顯示在 B300 上 ShareGPT @256 吞吐量達 8,530 tok/s，TPOT 僅 56.0 ms，假設解碼接受率約 67%。

## 結論
vLLM 的 MiniMax M3 首日支援不僅讓百萬 Token 多模態推理模型得以快速部署，更透過稀疏注意力核心、假設解碼與完整工具解析器，為代理工作載量（Agentic Workloads）提供兼具效能與實用性的推理基礎設施。
