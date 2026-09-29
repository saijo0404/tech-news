# Holo4: powering generalist computer-use agents

- **來源**: Hugging Face
- **發布日期**: 2026-09-28
- **原文連結**: https://huggingface.co/blog/Hcompany/holo4

## 核心主題
Holo4 是 Hugging Face 推出的新一代通用電腦使用代理模型，支援多種介面（GUI、程式碼、MCP、API），在學術 benchmarks 上表現優異，但更專注於實際商業工作流。

## 關鍵重點
- **雙版本設計**：提供 27B 稠密模型和 35B-A3B 專家混合模型，均透過 H Models API 提供
- **全介面支援**：支援 GUI、程式碼、MCP 和 API 介面，無需根據平台選擇不同模型
- **成本效益優異**：在 OSWorld 2.0 和 AutomationBench 等學術 benchmark 上與前沿模型競爭，但參數數量遠少於頂級模型
- **實際應用案例**：成功完成 3D 建模（Eiffel 塔）、H 公司 Logo 設計、Pac-Man 遊戲設計等專業軟體任務
- **訓練方法**：使用 Agentic Task Factory 產生大量任務進行監督學習和強化學習訓練
- **後續產品**：推出 Holotron4 Nano 作為後訓練堆疊，可將 Nemotron 3 Nano Omni 轉化為通用代理模型

## 結論
Holo4 是為實際商業應用設計的通用代理模型，在保持極低成本的同時提供強大的電腦操作能力，並透過開放原始碼和完整工具鏈讓開發者可以自訂和擴展。
---
