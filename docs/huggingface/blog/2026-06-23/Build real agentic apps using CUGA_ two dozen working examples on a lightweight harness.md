---
# Build real agentic apps using CUGA: two dozen working examples on a lightweight harness

- **來源**: Hugging Face Blog
- **發布日期**: 2026-06-23
- **原文連結**: https://huggingface.co/blog/ibm-research/cuga-apps

## 核心主題
IBM 發布 CUGA（Configurable Generalist Agent）——一個開源、模型無關的企業級 Agent 執行框架，內建治理、審批與策略功能，讓開發者只需撰寫工具清單與提示詞即可建構 AI Agent，且從筆記型電腦到符合主權要求的生產環境無需修改程式碼。

## 關鍵重點
- **框架取代框架外的框架（Harness）**：CUGA 反轉傳統 Agentic 開發流程——將規劃、反思步驟、變量追蹤與執行迴圈由框架承擔，模型不必自行修復錯誤。開發者只需四個引數建構 CugaAgent（模型、工具、特殊指示、狀態資料夾），支援 Fast / Balanced / Accurate 三種推理模式與 CodeAct 程式碼執行，即使使用較小開放權重模型（如 gpt-oss-120b）也能表現出色。
- **單一檔案應用程式與雙層工具架構**：24 個範例應用程式各僅需一個 FastAPI 檔案。工具分為兩類：MCP 工具（7 個公開伺服器、36 個通用無狀態能力如網頁搜尋、地理編碼、財務報價）與內聯工具（應用程式專屬 Python 函式，以 docstring 供 Agent 判斷呼叫時機）；統一回傳格式確保規劃器優雅處理錯誤。
- **治理內建、多 Agent 擴展與主權部署**：CUGA 內建六種策略類型（Intent Guard、Tool Approval、Tool Guide、Playbook、Output Formatter、CustomPolicy），以關鍵字或語意匹配觸發，策略版本控制於 `.cuga` 資料夾。多 Agent 方面，CugaSupervisor 可委派給 Specialist Agent，支援 A2A 外部委派，Agent Skills 按需載入 SKILL.md，ALTK-Evolve 讓 Agent 從自身執行中學習。透過 IBM Sovereign Core 邊界隔離，Agent 可部署於租戶自持環境中，所有資料與追蹤不外洩——治理是建構方式，不是事後補丁。

## 結論
CUGA 的核心價值在於「受治理是預設值」——將 Agentic 應用程式的基礎設施複雜性封裝成一個小 API，開發者專注於 Agent「能做什麼」而非「如何運作」。24 個共享骨架的範例應用程式提供從原型到生產的完整學習庫，從單一 Agent 到多 Agent 系統、從本地開發到企業級主權部署，一條路徑無需重寫。

---
