# Rebuilding AUTOMATIC1111 with Gradio Workflow

- **來源**: Hugging Face
- **發布日期**: 2026-09-10
- **原文連結**: https://huggingface.co/blog/gradio-workflow-1111

## 核心主題
這篇文章介紹了 Workflow1111，一個基於 Gradio Workflow 重建 AUTOMATIC1111 功能集的平台，包含 11 個媒體處理管道和 73 個節點。

## 關鍵重點
- Workflow1111 整合了 SOTA 模型，提供文字到圖像、高分辨率修復、圖像到圖像、提示矩陣、VLM 偵測、ControlNet 風格註釋器、背景移除、PNG 資訊儲存及圖像到影片等完整功能。
- 所有節點可透過 Hugging Face 帳號登入使用，模型調用會使用使用者自己的 quota，無需自行購買 GPU 硬體。
- 相比 ComfyUI，Workflow1111 提供零代碼 REST/MCP 端點，同時保持自定義節點的靈活性，所有輸出自動成為 API 端點。
- 支援本地 GPU 運行：透過 ZeroGPU 技術，可在本地機器上運行模型，無需依賴雲端服務。
- 可快速複製並修改工作流，或從小型工作流開始逐步擴展。

## 結論
Workflow1111 展示了 Gradio Workflow 如何通過圖形化節點編排，實現複雜的多模型 AI 工作流，無需手寫路由代碼即可構建可部署的 AI 應用。

---