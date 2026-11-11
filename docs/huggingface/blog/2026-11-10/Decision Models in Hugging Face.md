# Decision Models in Hugging Face

- **來源**: Hugging Face Blog
- **發布日期**: 2026-11-10
- **原文連結**: https://huggingface.co/blog/decision

## 核心主題
Hugging Face 推出的決策模型提供類型化介面與機率輸出，用於直接返回結構化決策而非生成文字，基於 System One 概念提供比傳統 LLM 更高效的決策能力。

## 關鍵重點
- **三種基本原語**：Choice(選擇)、Score(評分)、Noul(伯努利決策)，支援多種類型問題
- **機率輸出優勢**：提供機率分佈而非單一答案，避免 LLM 生成無效 JSON 的問題
- **統一推理介面**：透過 Transformers 和 llama.cpp 支援 /v1/systemone 端點，可透過 curl 發送請求
- **靈活性設計**：不強制共同實作，允許模型內部自由運作，只要符合相同狀態輸入、問題定義與決策返回的合約即可
- **模型轉換**：可將生成式 LLM 透過 LoRA 轉化為決策模型，支援 Trainer API 微調

## 結論
決策模型是 Hugging Face 生態系中快速發展的領域，提供類型化的介面與機率輸出，可透過 LoRA 微調生成式 LLM 實現，適用於請求分類、優先級評分及二元分類等場景。
---