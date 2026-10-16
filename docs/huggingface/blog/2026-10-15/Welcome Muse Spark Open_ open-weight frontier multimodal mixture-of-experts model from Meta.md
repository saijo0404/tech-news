# Welcome Muse Spark Open - Open-Weight Frontier Multimodal Mixture-of-Experts Model from Meta

- **來源**: Hugging Face Blog
- **發布日期**: 2026-10-15
- **原文連結**: https://huggingface.co/blog/meta-muse-spark-open

## 核心主題
Muse Spark Open 是 Meta 推出的 816B 參數開源權重多模態大語言模型，支援文本、圖像、音頻及視頻輸入，並具備自主代理行為能力。

## 關鍵重點
- **多框架支援與量化**：可部署於 llama.cpp、SGLang、vLLM、oMLX 等推理框架，提供 2-bit、3-bit、4-bit 及 NVFP4 量化版本以優化硬體效能
- **工具調用與自主代理**：支援函式調用（如 weather.get）可執行外部任務，採用 Harmony 通道式聊天模板支援自推理與工具調用路由
- **微調與部署**：可用 TRL 進行 LoRA 微調（64 GPU 訓練約 2 小時），支援 Hugging Face Inference Endpoints 提供 OpenAI 相容 API
- **多模態自主能力**：支援聲音輸入、視覺觀察與自主代理行為，可理解系統提示、網址與螢幕截圖但不處理 DOM/HTML 代碼
- **實際應用案例**：已開發 3D 資產生成、瀏覽器自動化、Amazon 產品搜尋等實例

## 結論
Muse Spark Open 是開源多模態大語言模型的重要里程碑，雖然需要大量資源（3-bit 量化仍需 256GB+ 記憶體），但為高階開發者提供了強大的部署基礎與廣泛的應用潛力。

---