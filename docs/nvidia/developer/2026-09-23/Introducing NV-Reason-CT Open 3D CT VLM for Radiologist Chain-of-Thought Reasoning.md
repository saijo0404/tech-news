# Introducing NV-Reason-CT Open 3D CT VLM for Radiologist Chain-of-Thought Reasoning

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-09-23
- **原文連結**: https://developer.nvidia.com/blog/introducing-nv-reason-ct-open-3d-ct-vlm-for-radiologist-chain-of-thought-reasoning/

## 核心主題
NVIDIA 推出 NV-Reason-CT，一款專為 3D CT 影像分析設計的視覺語言模型，具備放射科醫師式鏈式思維推理能力，可生成結構化診斷報告。

## 關鍵重點
- **架構創新**：結合全 3D 視覺轉換器編碼器與 Qwen3.5-4B 語言模型，原生處理 3D 體積數據，保留跨切片空間關係
- **推理能力**：模擬放射科醫師的鏈式思維推理，系統性審查解剖區域、識別異常、考慮鑑別診斷並表達 calibrated 不確定性
- **臨床優勢**：生成結構化診斷報告（涵蓋 30 種胸部、29 種腹部異常），支持多步驟對話跟進，提供可審計的推理過程
- **性能表現**：在 CT-RATE 基準測試上達致 SOTA 結果（Macro-F1: 0.614, Macro-AUROC: 0.871），超越所有現有 3D 對比及融合模型
- **開源定位**：非自主診斷系統，而是供研究者開發後訓練的開源基礎模型，可與 NVIDIA 醫療 AI 生態整合
- **訓練方法**：兩階段訓練（監督微調 + GRPO 強化學習），基於 55 萬個結構化 QA 範例訓練

## 結論
NV-Reason-CT 作為開源基礎模型，為放射學 AI 領域帶來突破性進展，可與 NVIDIA 醫療 AI 生態整合，協助開發者開發更精準的診斷工具，並通過 NIH 放射科醫師驗證報告品質與推理過程的臨床合理性。

---

**作者背景**：Andriy Myronenko（NVIDIA 資深研究科學家）、Supriya V. Thathachary（NVIDIA 醫療 AI 資深產品經理）、Monty Zarrouk（NVIDIA 醫療 AI 產品行銷主管）
