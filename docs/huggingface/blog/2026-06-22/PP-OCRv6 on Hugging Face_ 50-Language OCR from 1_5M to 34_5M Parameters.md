---
# PP-OCRv6 on Hugging Face: 50-Language OCR from 1.5M to 34.5M Parameters

- **來源**: HuggingFace Blog
- **發布日期**: 2026-06-22
- **原文連結**: https://huggingface.co/blog/PaddlePaddle/pp-ocrv6

## 核心主題
百度 PaddleOCR 團隊發布 PP-OCRv6——最新一代通用 OCR 模型系列，涵蓋從 1.5M 到 34.5M 參數的三種模型階梯，支援 50 種語言（含簡體中文、繁體中文、英文、日文與 46 種拉丁文字），提供精確的文字檢測與識別能力，適用於文件、截圖、多語影像、數位顯示與工業標籤等真實場景。

## 關鍵重點
- **三階梯模型設計與顯著效能提升**：（1）PP-OCRv6_tiny（1.5M 參數，檢測 Hmean 80.6%、識別準確率 73.5%）適用於邊緣裝置、輕量本地 OCR 與延遲敏感場景；（2）PP-OCRv6_small（7.7M 參數，檢測 84.1%、識別 81.3%）適合行動裝置、桌面端與多語 OCR 服務；（3）PP-OCRv6_medium（34.5M 參數，檢測 86.2%、識別 83.2%）面向精度導向與伺服器端管道。相較 PP-OCRv5_server，medium 版本文字檢測提升 +4.6 個百分點、文字識別提升 +5.1 個百分點。
- **全新架構升級：PPLCNetV4 骨干與 RepLKFPN 檢測**：三款模型共享 PPLCNetV4 作為統一的檢測與識別骨干網路，確保模型家族架構一致性。文字檢測模組升級為 RepLKFPN（輕量大型卷積特徵金字塔網路），針對多尺度文字（小字、密集、旋轉、低解析度、複雜背景）進行最佳化；識別模組採用 EncoderWithLightSVTR，結合局部上下文建模與全局注意力，改善多語文字、螢幕文字、工業字元與特殊符號的識別品質。
- **統一多語支援與多重推理後端**：medium 與 small 版本於單一模型內支援 50 種語言，減少多語場景中需維護多個獨立模型的需求。PaddleOCR 3.7 提供統一推理引擎介面，支援 Transformers（HuggingFace/PyTorch）、ONNX Runtime 與 Paddle Inference 三種後端，開發者可透過 `engine` 參數輕鬆切換，模型格式包含 safetensors、Paddle 推理模型與 ONNX 變體，方便整合至文件解析、RAG、搜尋與分析等下游系統。

## 結論
PP-OCRv6 透過統一的 PPLCNetV4 骨干網路、RepLKFPN 檢測模組與 EncoderWithLightSVTR 識別架構，在保持模型輕量化的同時實現了跨 50 種語言的高精度文字檢測與識別。從 1.5M 的邊緣 Tiny 模型到 34.5M 的伺服器 Medium 模型，搭配 Hugging Face Hub 上的多種格式與 PaddleOCR 的多後端支援，PP-OCRv6 為不同部署環境與應用場景提供了完整且靈活的 OCR 解決方案。

---
