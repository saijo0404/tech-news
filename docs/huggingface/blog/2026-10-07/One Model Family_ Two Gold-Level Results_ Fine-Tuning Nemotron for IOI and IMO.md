# One Model Family, Two Gold-Level Results: Fine-Tuning Nemotron for IOI and IMO

- **來源**: Hugging Face Blog
- **發布日期**: 2026-10-07
- **原文連結**: https://huggingface.co/blog/nvidia/nemotron-ioi-and-imo-2026

## 核心主題
NVIDIA 的 Nemotron 模型通過微調在國際資訊學奧林匹克(IOI)和國際數學奧林匹克(IMO)兩項競賽中都獲得金牌，證明其作為世界級專精模型的強大適應性。

## 關鍵重點
- **IOI 2026 金牌**：Nemotron-3-Ultra-CC 使用 SFT 和 GenCorrect 獲得 535.4/600 分，超過金牌門檻 361.12 分，並超越人類最高分 498.27 分
- **IMO 2026 金牌**：Nemotron 3 Ultra 使用 SFT 和 RL 在 generate-verify-refine 系統中獲得 30/42 分，超過官方金牌門檻 29 分，包含四題全分
- **可重用的微調方法**：四步驟方法（強基礎模型、精選問題、標準後訓練方法、推理迴路），無需為每個挑戰建立新基礎模型
- **資源開放**：所有模型、數據集和訓練方法都可在 Hugging Face 上獲取，包括 Nemotron-IMO-Bench 新 benchmark

## 結論
Nemotron 模型證明只需透過微調和透明推理工作流，即可將通用模型轉化為世界級領域專精模型，解決人類競賽前線問題。這些成果不僅適用於競賽，更具備廣泛的應用價值。
---

檔案已成功儲存至指定路徑。