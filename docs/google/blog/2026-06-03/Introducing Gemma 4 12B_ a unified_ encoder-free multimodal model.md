# 介紹 Gemma 4 12B：統一、無編碼器的多模態模型

- **來源**: Google Blog
- **發布日期**: 2026-06-03
- **原文連結**: https://blog.google/innovation-and-ai/technology/developers-tools/introducing-gemma-4-12b/

## 核心主題
Google DeepMind 推出 Gemma 4 12B，一款 120 億參數的統一多模態模型，採用無編碼器架構將視覺與音訊輸入直接融入 LLM 主幹，僅需 16GB VRAM 即可在消費型筆記型電腦本地運行，性能逼近更大的 26B MoE 模型。

## 關鍵重點
- **創新統一架構：徹底移除多模態編碼器**：傳統多模態模型依賴獨立編碼器先將影像與音訊轉換為表示再送入語言模型，Gemma 4 12B 以無編碼器架構將視覺輸入替換為輕量嵌入模組（單一矩陣乘法、位置嵌入與歸一化），音訊輸入則完全移除編碼器、將原始音訊訊號直接投影至與文字 token 相同的維度空間，由 LLM 主幹直接處理多模態輸入，降低延遲並減少記憶體佔用。
- **筆電級效能與代理式工作流**：在標準基準測試中，Gemma 4 12B 的性能逼近更大的 26B MoE 模型，但記憶體總佔用不到一半；僅需 16GB VRAM 或統一記憶體即可在消費型筆電本地運行，支援強大的多步推理與代理式（agentic）工作流程；同時內建多 token 預測（MTP）草稿器以降低推理延遲。自 Gemma 4 系列推出以來，開發者社群已突破 1.5 億次下載，應用涵蓋穿戴式機械臂與企業級 AI 安全等領域。
- **全面開放與生態系整合**：模型以 Apache 2.0 授權釋出，支援 LM Studio、Ollama、Google AI Edge 等多個開發工具與推理框架（Hugging Face Transformers、llama.cpp、MLX、SGLang、vLLM），並可透過 Unsloth 進行高效微調；Google 同時釋出官方 Skills Repository 讓代理程式能直接使用 Gemma 最新能力；部署方面支援 Google Cloud 的 Gemini Enterprise Agent Platform Model Garden、Cloud Run 與 GKE。

## 結論
Gemma 4 12B 以「無編碼器統一架構」打破多模態模型的效率瓶頸，將逼近大模型性能的推理能力帶入一般筆電，搭配全面開放授權與豐富的開發生態系，為本地化代理式 AI 應用開啟新紀元。
