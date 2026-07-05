# Interactions API: our primary interface for Gemini models and agents

- **來源**: Google Blog
- **發布日期**: 2026-06-22
- **原文連結**: https://blog.google/innovation-and-ai/technology/developers-tools/interactions-api-general-availability/

## 核心主題
Google DeepMind 宣布 Interactions API 正式通用（GA），作為 Gemini 模型與 Agent 的主要介面——提供單一統一的端點，支援伺服器端狀態管理、背景執行、工具組合與多模態生成，簡化開發者建構 Gemini 應用的流程。

## 關鍵重點
- **Managed Agents 與背景執行**：透過單一 API 呼叫即可配置遠端 Linux 沙箱（預設搭載 Antigravity Agent），讓 Agent 自主推理、執行程式碼、瀏覽網頁與管理檔案；任何呼叫均可設定 `background=True` 以非同步方式在伺服器端執行長途任務。工具方面，可混合使用內建工具（Google Search、Google Maps）與自訂函數，且工具結果可同時回傳圖片與文字。
- **Deep Research 升級與多模態生成**：提供兩種 Agent 版本（速度優先 vs. 深度優先）、協同規劃、原生圖表與資訊圖表生成，以及支援圖片、PDF 與音訊的多模態錨定。媒體生成部分，新增 Nano Banana 2 影像生成、Google Image Search 錨定、Lyria 3 音樂生成，以及支援多說話者的表情化語音合成。
- **開發者體驗與生態系整合**：架構從「角色」簡化為「步驟」（每個動作如 user_input、thought、function_call 皆為獨立型別），Flex 與 Priority 兩種層級可優化成本（Flex 降價 50%）或延遲，錯誤訊息能精確指出問題欄位，付費層保留 55 天歷史紀錄。API 已成為 Google AI Studio、Gemini API 與所有文件預設，並推出 gemini-interactions-api Skill 為編碼 Agent 自動注入最佳實踐；Python 與 JavaScript SDK 已支援，LiteLLM、Eigent、Agno 等第三方框架也已完成整合。

## 結論
Interactions API 是 Google DeepMind 從開發者回饋中誕生的 Agent 優先介面——將模型推理與 Agent 工作流統一在單一設計良好的 API 中，取代傳統無狀態的 generateContent 模式。雖然舊版 API 仍受支援並持續獲得新模型，但長期來看，前端能力與 Agent 功能將逐步集中在 Interactions API，Google 希望它成為第三方 SDK 與函式庫的預設標準。

---
