# Nemotron 3.5 Content Safety: Customizable Multimodal Safety for Global Enterprise AI

- **來源**: Hugging Face Blog (NVIDIA)
- **發布日期**: 2026-06-04
- **原文連結**: https://huggingface.co/blog/nvidia/nemotron-3-5-content-safety

## 核心主題
NVIDIA 發布 Nemotron 3.5 Content Safety，一款基於 Gemma 3 4B 的單一多模態、多語言安全分類模型，首次整合自訂企業政策執行與可稽核推理軌跡，在 8GB VRAM GPU 上實現低延遲即時內容安全審核。

## 關鍵重點
- **五項核心能力**：（1）統一多模態評估——一次性處理提示詞、圖片與回應的完整上下文窗口，捕捉單一輸入無法發現的交互風險；（2）全球語言覆蓋——12 種明確訓練語言加上約 140 種零樣本泛化；（3）自訂政策執行——模型接受自然語言自訂政策規範並在推理時動態解釋，支援類別停用與自訂風險類別注入；（4）思考模式（THINK Mode）——可選的逐步推理軌跡，以兩步壓縮至 3 句以控制延遲；（5）公開安全資料集——包含真實影像（99% 非合成）、多語言與推理軌跡。
- **效能與延遲優勢**：在多語言 Aegis 上達 96.5% 準確率、RTP-LX 上 88.8%，整體多模態基準平均約 85%；與 LlamaGuard-4-12B 相比延遲僅約一半，與推理安全模型相比在思考模式下少產生 50% token，滿足 13 項 Aegis 核心類別加 10 項子類別的完整分類需求。
- **資料集與基準缺口應對**：訓練資料結合 Nemotron Safety Guard Dataset v3、NVIDIA 人工標註多模態資料（含 Wikimedia 真實影像）、VLM Dataset v2、Qwen 397B/80B 教師模型生成的推理軌跡，以及 CantTalkAboutThis 政策規範資料；文章同時指出多模態安全研究的三大基準缺口（純文字覆蓋不足、合成影像品質偏低、真實影像授權限制）仍是社群待解難題。

## 結論
Nemotron 3.5 Content Safety 以單一 4B 模型在 8GB+ GPU 上提供多模態、多語言、自訂政策與可稽核推理的企業級內容安全方案，支援 transformers、vLLM 與 SGLang，並已部署於 NVIDIA NIM 與 Baseten、DeepInfra 等推理平台，以 NVIDIA Open Model License 開放研究與商業使用。

---
