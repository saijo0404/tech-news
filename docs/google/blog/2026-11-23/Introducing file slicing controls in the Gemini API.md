# Introducing file slicing controls in the Gemini API

- **來源**: Google Blog
- **發布日期**: 2026-11-23
- **原文連結**: https://blog.google/innovation-and-ai/technology/developers-tools/file-slicing-controls/

## 核心主題
Gemini API 新增原生檔案切片控制功能，開發者可指定模型需載入的特定頁面、表格範圍與媒體片段，大幅降低大檔案的 token 成本。

## 關鍵重點
- 支援 PDF、Office 檔案（Word、Excel、PowerPoint）、音頻與視頻的直接上傳與處理
- 可精確指定頁面範圍、工作表範圍、時間段及解析度等參數
- 採用「先概覽後深入」策略：先以低成本提取文字概覽，再對重點內容使用高解析度處理
- 由伺服器端自動完成切片、渲染與分詞，避免客戶端本地負載（如 LibreOffice、PDF 渲染器等）

## 結論
透過檔案切片控制，開發者能更精準地控制模型處理範圍，降低 token 消耗並提升多輪工作流的效率，同時減少客戶端資源負擔。

---