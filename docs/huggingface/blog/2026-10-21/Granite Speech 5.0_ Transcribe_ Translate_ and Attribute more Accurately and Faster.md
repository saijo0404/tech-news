# Granite Speech 5.0: Transcribe, Translate, and Attribute more Accurately and Faster

- **來源**: Hugging Face
- **發布日期**: 2026-10-21
- **原文連結**: https://huggingface.co/blog/ibm-granite/granite-speech-5

## 核心主題
IBM 推出了 Granite Speech 5.0 系列的三個模型更新，涵蓋高準確度多語言語音識別、快速邊緣端語音識別以及多說話者會議記錄等企業級語音處理需求。

## 關鍵重點
- **granite-speech-5.0-2b**：新的多語言語音模型，支援英、法、德、西、葡、日六種語言，提供翻譯功能，支援最多 2,000 個詞彙的關鍵字偏置，可要求標點符號和大小寫格式化輸出。
- **granite-speech-5.0-470m-turboctc**：經過更新的快速語音識別模型，支援多語言識別，具備原生標點符號和大小寫功能，比原版快 1.6 倍，適合邊緣端高速處理。
- **granite-speech-4.1-2b-plus**：針對多說話者會議和通話優化的模型，大幅提升了說話者歸屬準確度（WDER 降低 7%）、時間戳記精度（AAS 降低超過一半）以及長語音表現（WER 降低 24%）。

## 結論
這三項更新共同構成了完整的企業語音解決方案，涵蓋從高準確度翻譯到快速邊緣處理的全方位需求，並採用 Apache 2.0 授權，可透過 Transformers、vLLM 等多個平台部署。
