# Building a Haunted House with NVIDIA Nemotron Open Models

- **來源**: Hugging Face Blog
- **發布日期**: 2026-10-30
- **原文連結**: https://huggingface.co/blog/nvidia/nemotron-halloween

## 核心主題
作者 Rick Grandy 利用 NVIDIA Nemotron 系列開源模型，打造了一個互動式萬聖節「鬼屋」投影系統，讓小鬼能與它互動，並根據禮貌程度改變反應。

## 關鍵重點
- **聽覺與視覺**：使用 NVIDIA Nemotron 3 ASR 聆聽訪客，Nemotron 3 Nano Omni 識別萬聖節服裝，YOLO 和 ByteTrack 追蹤訪客。
- **思考與對話**：核心由 NVIDIA Nemotron 3.5 Bolt E4B 4GB 驅動，搭配 LoRA 微調以塑造「暴躁海盜船」性格。
- **聲音合成**：NVIDIA Magpie TTS Zeroshot 將文字轉為聲音，Audio2Face-3D 驅動木門口的動畫。
- **系統架構**：雙 GPU 架構（RTX PRO 6000 Blackwell Max-Q 處理語言模型，RTX PRO 4000 Blackwell 處理圖形），可在單一工作站運行。
- **互動邏輯**：鬼屋初始態度惡劣，但若訪客說「請」會軟化態度，並給予糖果。

## 結論
這是一個展示 NVIDIA Nemotron 系列模型實戰應用的完整案例，證明了開源 AI 模型在本地化、低成本互動系統中的巨大潛力。作者鼓勵讀者使用 Nemotron Voice Agent 框架自行構建個性化角色。
---
