# Granite Switch 4.1.1 — Update models like you update software

- **來源**: Hugging Face
- **發布日期**: 2026-10-29
- **原文連結**: https://huggingface.co/blog/ibm-granite/granite-switch-4-1-1

## 核心主題
IBM Granite 發布了 Granite Switch 4.1.1 更新版本，展示了其模組化架構的優勢，允許像更新軟體一樣更新模型。

## 關鍵重點
- 更新了 Granite Speech ASR 模型，支援10種語言的多語言語音轉文字，並具有原生標點和大小寫功能，使轉錄結果可直接供後續模型使用
- 更新了 granitelib-core 中的決策適配器，在 Jev 決策指數測試集上表現更好
- 更新過程完全後向相容，不需要遷移，基礎模型未重新計算，僅訓練新的 ASR 模型和決策適配器

## 結論
這種模組化架構允許開發者快速迭代和部署更新，未來將推出教程和 Adapter SDK，讓開發者和第三方提供者可以建立自己的適配器，實現像軟體開發般的敏捷更新模式。
---
