# Build Anything with gr.Workflow

- **來源**: Hugging Face
- **發布日期**: 2026-08-25
- **原文連結**: https://huggingface.co/blog/gradio-workflow-guide

## 核心主題
這篇文章介紹了 Gradio 的 gr.Workflow 功能，讓使用者可以透過圖形化介面輕鬆構建 AI 工作流管道，無需手寫複雜的程式碼。

## 關鍵重點
- **圖形化工作流構建**：使用者可以透過拖曳式介面將輸入、操作和輸出連接成工作流圖，每個節點都是可執行的
- **多種操作類型支援**：支援自己的 Python 函數、Hugging Face 推理提供者、Gradio Spaces 或 Hub 數據集
- **自動 API 端點**：每個工作流輸出自動成為 REST API 端點，可透過程式碼直接調用
- **並行處理能力**：支援 fan-out 模式，單一輸入可同時驅動多個並行操作
- **GPU 模型運行**：透過 @spaces.GPU 裝飾可運行本地 GPU 模型，無需依賴外部推理服務

## 結論
gr.Workflow 大幅簡化了 AI 應用開發流程，讓開發者可以透過直觀的圖形介面快速構建複雜的工作流，並自動獲得可部署的 API 服務。

---