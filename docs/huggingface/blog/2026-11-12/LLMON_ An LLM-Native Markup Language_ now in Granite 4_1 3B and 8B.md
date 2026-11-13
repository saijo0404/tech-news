# LLMON: An LLM-Native Markup Language, now in Granite 4.1 3B and 8B

- **來源**: Hugging Face
- **發布日期**: 2026-11-12
- **原文連結**: https://huggingface.co/blog/ibm-granite/llmon-an-llm-native-markup-language-now-in-granite

## 核心主題
LLMON 是一種專為大語言模型設計的標記語言，透過明確的結構化語法增強模型對指令、資料與限制條件的理解能力，同時大幅降低提示注入攻擊風險。

## 關鍵重點
- **LLMON 架構優勢**：使用保留的特殊 token 作為分隔符，結構與內容使用 vocab 不同部分，比 JSON 更適合因果語言模型，解決了 JSON 結構對模型難以理解的問題。
- **指令/資料分離機制**：透過明確區分指令與資料，並使用 unique ID 綁定執行區塊，有效防止間接提示注入攻擊，測試中攻擊成功率降低 95% 以上。
- **實驗性模型發布**：推出 granite-4.1-3b-LLMON-preview 和 granite-4.1-8b-LLMON-preview 兩個預覽模型，基於 Granite 4.1 基模型訓練，支援 LLMON 格式。
- **與聊天模板兼容**：LLMON 不取代聊天模板，而是增強它們，模型仍可透過 apply_chat_template 使用，只需在訊息中標記各部分為 exec: True/False。
- **無損轉換工具**：提供 JSON 到 LLMON 的轉換工具，團隊已有 JSON 工作流的團隊可無痛轉換。
- **可自訂語法**：支援自訂標籤和結構，可針對特定領域（如 ScienceWorld）訓練 LoRA 適配器。

## 結論
LLMON 代表大語言模型結構化輸入的重要進展，特別適合需要高可靠性的應用場景。雖然目前為實驗性預覽版本，但已顯示出在保持一般能力的同時大幅提升安全性的潛力，建議開發者可先透過 Mellea 工具進行測試評估。
---
