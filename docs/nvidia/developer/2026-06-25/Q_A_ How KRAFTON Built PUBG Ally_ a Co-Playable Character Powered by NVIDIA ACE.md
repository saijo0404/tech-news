---
# Q&A: How KRAFTON Built PUBG Ally – a Co-Playable Character Powered by NVIDIA ACE

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-06-25
- **原文連結**: https://developer.nvidia.com/blog/how-krafton-built-pubg-ally-a-co-playable-character-powered-by-nvidia-ace/

## 核心主題
KRAFTON 與 NVIDIA 合作開發 PUBG Ally——全球首款「可共同遊玩角色」（Co-Playable Character, CPC），基於 NVIDIA ACE 架構，結合自動語音辨識、2B 參數小型語言模型與自研語音合成技術，讓 AI 隊友能在《PUBG: BATTLEGROUNDS》中理解玩家語音、即時推理遊戲情境並做出自然回應。

## 關鍵重點
- **雙層架構：System 1 快速反應與 System 2 深度推理**：PUBG Ally 採用類似人類決策的雙層設計——System 1 以行為樹處理即時遊戲動作（移動、射擊、戰鬥反應），以遊戲 tick rate 執行從不等待語言推理；System 2 則由在地的 Mistral-NeMo-Minitron-2B 小型語言模型負責解讀玩家意圖、協調溝通與生成自然語音。這種分工確保戰鬥反應零延遲，同時保留 AI 隊友的自然互動能力。
- **端側部署與延遲優化**：選擇 2B 參數小型語言模型而非雲端大模型，是為了消除網路往返延遲、確保即時響應。模型經過量化後可在僅 8GB VRAM 的 GPU 上運行，且透過 KV cache 優化——穩定指令與遊戲情境跨輪次保持一致，僅更新最相關的即時資訊。 Ally 透過工具呼叫主動觀察遊戲引擎數據（自身狀態、隊友位置、附近物品、戰鬥情況），確保所有回應基於最新的事實而非模型猜測。
- **領域適應與長期記憶**：Ally 的世界觀被限制在單一地圖（Sanhok）與單一模式（AI Duo），搭配確定性的 PUBG 規範與工具驅動的知识查閱，確保術語與行為準確。記憶系統分為兩層——跨對局的長期記憶（玩家名稱、偏好武器、降落地點）與局內的短期記憶（近期語音與遊戲事件），讓 Ally 從單局助手蛻變為能認得玩家、主動呼喚名字的持久隊友。

## 結論
PUBG Ally 代表了遊戲 AI 從腳本式 NPC 邁向真正可共同遊玩角色的里程碑。KRAFTON 的經驗證明，在資源受限的端側環境中，小型語言模型與精心設計的雙層架構結合，能在延遲、可用性和自然度之間取得最佳平衡。其「快速原型→大量玩家測試→迭代」的循環方法，以及跨對局記憶的建立，為遊戲產業開發 AI 夥伴提供了可複製的範例，展現了 AI 如何重新定義多人遊戲中的合作體驗。

---
