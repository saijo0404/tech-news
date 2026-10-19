# Scaling Indic Pretraining

- **來源**: Hugging Face Blog
- **發布日期**: 2026-10-16
- **原文連結**: https://huggingface.co/blog/nvidia/scaling-indic-pretraining

## 核心主題
NVIDIA 與 IIT Madras AI4Bharat 實驗室合作推出 Nemotron-pretraining-Indic-v1 數據集，包含約 2.8 兆 token，涵蓋印度憲法列出的 22 種語言，並提供開源 GPU 加速數據生成管道。

## 關鍵重點
- 數據集包含 2,6010 億 native-script token 和 2,246 億 romanized token，涵蓋 34 種語言-書寫系統配置
- 使用 NeMo Data Designer 框架進行翻譯、質量評估與修復，每個記錄可追溯至原始文檔來源
- Nemotron 3.5 Super VL 在 Indic 知識與推理 benchmarks 上全面提升，5 項指標提升 4.98% ~ 9.82%
- 提供開源 GPU 加速數據生成管道，可透過 Hugging Face Datasets 直接下載

## 結論
此數據集為印度語言大語言模型訓練提供高品質開源資源，並通過自動化質量控制流程確保數據可靠性，同時支持未來擴展至更多印度語言模型開發。
---