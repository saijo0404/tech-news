# 介紹 Gemma 4 12B：統一的無編碼器多模態模型

- **來源**: Google DeepMind Blog
- **發布日期**: 2026-06-03
- **原文連結**: https://deepmind.google/blog/introducing-gemma-4-12b-a-unified-encoder-free-multimodal-model/

## 核心主題
Google DeepMind 發布 Gemma 4 12B——首款支援原生語音輸入的中型多模態模型，以無編碼器統一架構將視覺與語音輸入直接整合至 LLM 後端，在僅需 16GB VRAM 的消費型筆記型電腦上即可本地運行，並達到逼近更大 26B MoE 模型的推理效能。

## 關鍵重點
- **創新統一架構：無多模態編碼器，視覺與語音直接流入 LLM 主幹**：傳統多模態模型通常依賴獨立編碼器將圖像與語音翻譯為表示後再傳遞給語言模型，這些分離編碼器增加延遲與記憶體使用；Gemma 4 12B 採用無編碼器架構，將視覺與語音輸入直接整合——（1）視覺：以單一矩陣乘法、位置嵌入與歸一化組成的輕量嵌入模組取代 Gemma 4 的視覺編碼器，讓 LLM 主幹直接接管視覺處理；（2）語音：進一步簡化，完全移除語音編碼器，將原始語音信號投射至與文字 token 相同的維度空間；這使Gemma 4 12B成為Gemmas 4系列首款原生支援語音輸入的中型模型。
- **效能接近 26B 模型、本地運行只需 16GB 記憶體：推動 Agent 開發普及**：Gemma 4 12B 在標準基準測試上的效能接近更大的 26B MoE 模型，但記憶體佔用不到一半，足以在配備 16GB RAM 或統一記憶體的消費型筆記型電腦上本地運行，解鎖強大的多模態與代理式（agentic）體驗；同時支援 Multi-Token Prediction（MTP）草稿器以降低推論延遲；Gemma 4 系列模型累積已超過 1.5 億次下載，開發者社群已建構出從穿戴式機械臂到企業級 AI 安全等多樣化應用。
- **開放授權與全生態系工具支援：從 LM Studio 到 Google Cloud 一應俱全**：以 Apache 2.0 授權發布，支援跨開發者生態系——（1）立即體驗：LM Studio、Ollama、Google AI Edge Gallery App、Google AI Edge Eloquent App、LiteRT-LM CLI；（2）下載權重：Hugging Face 與 Kaggle；（3）整合與學習：Hugging Face Transformers、llama.cpp、MLX、SGLang、vLLM、Unsloth 微調；（4）代理開發：官方 Skills Repository（gemma-skills）提供專為 Agent 建構設計的技能庫；（5）生產部署：Gemini Enterprise Agent Platform Model Garden、Cloud Run、GKE。

## 結論
Gemma 4 12B 代表開放多模態模型的重要里程碑——以無編碼器統一架構消除傳統多模態模型的編碼器瓶頸，在 12B 參數量下實現逼近 26B MoE 模型的推理能力，同時將運行門檻降至消費型筆記型電腦的 16GB 記憶體；加上原生語音輸入支援、MTP 草稿器加速、以及從本地工具到雲端部署的全方位生態系覆蓋，Gemma 4 12B 讓高階多模態 AI 真正走進個人裝置，為開發者與終端使用者提供在本地建構智能代理與多模態應用的新選擇。
