# 如何使用 NVIDIA MCG Toolkit 自動化 AI 模型文件化

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-05-29
- **原文連結**: https://developer.nvidia.com/blog/how-to-automate-ai-model-documentation-with-the-nvidia-mcg-toolkit/

## 核心主題
NVIDIA 模型卡產生器（MCG Toolkit）是一套容器化管線，能自動從模型原始碼讀取資訊、生成符合 Model Card++ 標準的完整模型文件，將耗時的文件化過程縮短至一分钟內。

## 關鍵重點
- **三段式自動化管線**：MCG Toolkit 透過「攝取（Ingestion）→ 擷取（Extraction）→ 渲染（Rendering）」流程，讀取 GitHub、GitLab 或 HuggingFace 等原始碼倉庫，利用 NVIDIA Nemotron RAG 進行高精準嵌入與重新排序，再由 GPT-OSS-120B 生成符合規範的模型卡概覽與四個子卡（偏見、可解釋性、隱私、安全與安全）。
- **高度可自訂與靈活性**：工具不綁定特定模型、模板或標準，使用者可自訂 LLM 端點、輸出模板與領域知識庫，並支援 CycloneDX 合規格式；當新法規出現時，只需更新模板而不需修改核心程式碼。
- **效能與實際應用**：在標準化測試中，NVIDIA Nemotron Nano 8B 僅需 56 秒即可生成 97% 完成率與 92% 準確率的模型卡；Oracle 已將其整合至 OCI AI 生產環境，作為 AI 透明度的核心工具，並能精準標示文件缺口供人工審查。

## 結論
MCG Toolkit 讓 AI 模型文件化跟上模型開發速度，無論團隊文件齊全還是正在完善，都能自動生成合規、可審核的模型卡，配合開源的 Model Card++ 模板，為 AI 透明度提供實用的基礎建設。
