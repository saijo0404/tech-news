---
# How an Agent Built a 3D Paris Gallery by Chaining Two Hugging Face Spaces

- **來源**: Hugging Face Blog
- **發布日期**: 2026-06-09
- **原文連結**: https://huggingface.co/blog/mishig/spaces-agents-md

## 核心主題
Hugging Face 工程師 mishig 展示如何透過 coding agent 串接兩個 Spaces（Ideogram 4 圖像生成與 TripoSplat 3D 重建），僅用提示詞就完整產出一座巴黎景點 3D 高斯潑溅展示網站，無需人工操作任何模型或工具。

## 關鍵重點
- **agents.md 讓每個 Space 成為建築模組**：Gradio Space 自動暴露純文字格式的 agents.md，包含 API schema、呼叫模板、檔案上傳方式與驗證提示，agent 只需讀取並設定 HF_TOKEN 即可驅動整個 Space，實現「提示 → 圖像 → 3D」的零程式碼鏈接。
- **從巴黎到日本、埃及的模板化擴展**：確認管道後，僅更改提示詞，agent 就能在約一句話的費用內複製出埃及與日本的同等展示，完整產生六張圖像、六個 3D splat、壓縮為 .ksplat、搭建 Three.js 互動檢視器並部署，展現模組經濟中「多邊際成本趨近於描述成本」的現象。
- **Agent 偏好已記錄且可達的資源**：agents.md 讓 Spaces 變得比需要手動設定 SDK、權重與 GPU 的模型更吸引 agent，正如 Mitchell Hashimoto 描述的「建築模組經濟」——AI 擅長的不是從零建構，而是將經過驗證的模組黏合在一起；Hugging Face Hub 的開源權重目錄已轉化為可呼叫的多媒體原語庫。

## 結論
這篇文章不僅是一個展示作品，更預示了多媒體軟體的未來開發方式：當每個模型都成為可被 agent 讀取與串接的模組時，「把提示轉成旋轉 3D 景點」不再是專案，而只是管道中的一個步驟。

---
