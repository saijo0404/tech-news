---
# We got local models to triage the OpenClaw repo for FREE!*

- **來源**: Hugging Face Blog
- **發布日期**: 2026-06-22
- **原文連結**: https://huggingface.co/blog/local-models-pr-triage

## 核心主題
Hugging Face 團隊利用本地開放權重模型（Gemma-4-26B、Qwen3.6-35B）搭配 Agent 執行框架，建構零成本（僅電費）的即時 PR/Issue 分類系統，在 330 筆評估集上達到 F1 分數 0.80-0.82，證明中型本地模型無需微調即可高效分類，並可擴展至新聞分類、客服工單篩選等多個領域。

## 關鍵重點
- **本地模型分類架構與安全性設計**：系統使用 Pi Agent 執行框架驅動本地模型，接收 PR 標題、內文與差異檔摘要後進行分類。模型可使用受限的 `reposhell`（只讀命令如 ls、grep、git 等）自行探索程式碼庫以驗證標籤（例如：原本認為是 coding_agent_integrations，透過檢查 package.json 更正為 inference_api）。分類結果透過 `final_json` 工具輸出至固定 Schema。架構採用半 Agent 模式：分類由 Agent 完成、通知由確定性規則處理，節省 GPU 資源。
- **模型效能比較**：在 330 筆人工標籤評估集（3x GPT-5.5 + 2x Opus 4.8 交叉標記）上測試三種模型——Gemma-4-26B-A4B（F1 0.80，召回 0.91，精確度 0.72，每行 1.4 秒）、Qwen3.6-35B-A3B（F1 0.82，召回 0.82，精確度 0.83，每行 13.5 秒）、DeepSeek-V4-Flash（F1 0.81，但每行 144 秒不切實可行）。Gemma 速度快、召回率高但誤報較多（227 筆 vs Qwen 的 106 筆）；Qwen 精確度高、誤報少但速度較慢。Gemma 使用 vLLM + NVFP4 量化、並行 16 在 GB10 上達每秒 403 聚合輸出 token。
- **即時驗證與可擴展應用**：每兩小時以 GPT-5.5 作為裁判比對本地模型的誤報與漏報，自動更新報告至 GitHub，並在 Discord 通知。這種「高吞吐量分類」架構可應用於新聞分類、社群帖子篩選、客服工單分流、內容審核上訴、業務外展篩選、arXiv 論文過濾等多領域。Agent 分類（agentic classification）的優勢在於模型不需一次性讀取所有資訊，可主動搜尋上下文後再返回結構化資料。

## 結論
這篇實證展示了本地開放權重模型在 2026 年的實用性：無需雲端 API 費用、無需微調，中型模型即可在特定領域達到與雲端 SOTA 模型接近的分類效能。配合 Agent 執行框架與受限 shell 的安全設計，本地模型分類系統不僅降低成本，更確保資料自主與即時性。對於任何需要高吞吐量資訊過濾的場景，這提供了一條可立即實踐的開源路徑。

---
