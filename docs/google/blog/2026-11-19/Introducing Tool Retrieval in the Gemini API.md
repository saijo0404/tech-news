# Introducing Tool Retrieval in the Gemini API

- **來源**: Google Innovation & AI Blog
- **發布日期**: 2026-11-19
- **原文連結**: https://blog.google/innovation-and-ai/technology/developers-tools/gemini-api-tool-retrieval/

## 核心主題
Google 推出 Gemini API 的 Tool Retrieval 功能，讓代理可以按需載入工具參數模式，減少輸入 token 和延遲，提升大型工具庫管理效率。

## 關鍵重點
- **按需載入工具參數**：代理保持完整工具庫待命，只在需要時載入特定工具的參數模式，避免每次請求都傳送完整工具庫。
- **減少 token 消耗與延遲**：通過只載入必要工具的參數模式，顯著降低輸入 token 計數和請求延遲。
- **提高工具選擇準確性**：當工具庫規模擴大時，Tool Retrieval 能保持工具選擇的準確性，避免因工具列表過長而影響模型判斷。
- **支援 Gemini 3.6 及更高版本**：此功能適用於 Gemini 3.6 及所有 Gemini 4 系列模型，可在 Interactions API 中使用。
- **啟用方式簡單**：只需在請求中添加 `tool_search` 工具，並將需要延遲載入的工具設置 `defer_loading: true`。
- **支援遠端 MCP 伺服器**：可將整個 MCP 伺服器工具集延遲載入，無需逐一列出工具。
- **與前綴快取兼容**：延遲載入的工具模式不會影響快取前綴，保持對話一致性。

## 結論
Tool Retrieval 是管理大型工具庫的有效解決方案，讓開發者能更輕鬆地構建高效、準確且成本效益的 AI 代理應用。此功能已開放預覽，可立即在 Gemini Interactions API 中嘗試使用。

---