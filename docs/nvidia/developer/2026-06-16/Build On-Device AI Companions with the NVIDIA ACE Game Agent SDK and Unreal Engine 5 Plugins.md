---
# Build On-Device AI Companions with the NVIDIA ACE Game Agent SDK and Unreal Engine 5 Plugins

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-16
- **原文連結**: https://developer.nvidia.com/blog/build-on-device-ai-companions-with-the-nvidia-ace-game-agent-sdk-and-unreal-engine-5-plugins/

## 核心主題
NVIDIA 宣布推出 ACE Game Agent SDK Beta 與一組全新 Unreal Engine 5 插件，讓遊戲開發者能直接在設備端（on-device）建構具備自然語音互動與即時反應的 AI 夥伴（NPC），全面運行於 GeForce RTX 硬體上。

## 關鍵重點
- **ACE Game Agent SDK 三大核心 API**：Agent API（維護聊天歷史、自主驅動多步驟工具推理）、Chat API（無狀態直接控制推論）、RAG API（從開發者自建資料庫進行語意/詞彙/混合檢索，確保回答基於最新知識）。該 SDK 已在《Total War: PHARAOH》實戰驗證——以古埃及法老為形象的遊戲內 AI 顧問，透過 RAG 架構查詢 1,200+ 張關聯遊戲資料表，即時回答玩家策略問題。
- **Unreal Engine 5 三合一 AI 插件套件**：包含自動語音辨識（ASR，內建 nemo-conformer-ctc-120m 英文模型並支援 7 種額外語言）、小型語言模型（SLM，支援 GGUF 格式，內建 Qwen 3.5 4B 模型用於低延遲對話與函數呼叫）、以及文字轉語音（TTS，內建 Chatterbox Turbo 350M 高品質模型與範例聲音）。所有模型均在本地 RTX 硬體運行，避免雲端服務的延遲與不確定成本。
- **DLSS 4.5 插件與 Unreal Fest 2026 新成果**：DLSS 4.5 插件支援動態多幀生成（6X 模式）與第二解析度超解析 Transformer；Unreal Fest 上展示 KRAFTON 的 PUBG AI 隊友 Ally、Animotive Kimodo UE 插件（透過自然語言提示生成可控人類動作）、以及 SOKRISPYMEDIA 以雙 RTX PRO 6000 Blackwell 工作站訓練手繪武器客製化模型的案例。

## 結論
NVIDIA 透過 ACE Game Agent SDK 與 UE5 插件的開放，將雲端 AI NPC 的架構拉回設備端，使遊戲開發者能以低延遲、可控成本的本地化方式打造深度互動的 AI 夥伴。搭配 DLSS 4.5 與 Kimodo 等工具，AI 正從「遊戲內容」轉變為「遊戲體驗的核心驅動力」，重新定義 NPC 的角色與玩家互動的可能性。

---
