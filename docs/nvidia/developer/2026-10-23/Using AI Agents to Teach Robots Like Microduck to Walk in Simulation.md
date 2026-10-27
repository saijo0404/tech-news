# Using AI Agents to Teach Robots Like Microduck to Walk in Simulation

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-10-23
- **原文連結**: https://developer.nvidia.com/blog/using-ai-agents-to-teach-robots-like-microduck-to-walk-in-simulation/

## 核心主題
這篇文章介紹了如何使用 AI 代理（AI Agents）在模擬環境中教導 Microduck 機器人學習行走和避障，涵蓋從資產創建、環境組裝到策略訓練與驗證的完整工作流程。

## 關鍵重點
- **AI 代理協作**：NVIDIA RTX Spark 作為本地開發中心，Hermes 和 Nemotron 3.5 Bolt 將提示轉換為逐步項目計劃，Astra 則負責創建 3D 模擬資產
- **資產創建流程**：使用雲端圖片編輯提升參考影像品質，透過 FreeCAD 建模和 Blender 材質應用生成可編輯模型與 USD 資產
- **模擬環境組裝**：在 NVIDIA Isaac Sim 中組裝障礙賽道，結合 Omniverse 庫的渲染與傳感器模擬，以及 Newton 的物理引擎模擬 Microduck 的運動與平衡
- **策略訓練與驗證**：NVIDIA Isaac Lab 在 4,096 個並行環境中訓練感知與運動策略，使用 NVIDIA RTX PRO 6000 Blackwell GPU，訓練後策略在 RTX Spark 上進行驗證
- **模擬到實體部署**：透過 Better Actuator Models 和領域隨機化技術縮小模擬與現實差距，為實體機器人部署奠定基礎

## 結論
這個工作流程展示了 AI 代理如何協同完成從概念設計到策略驗證的完整機器人開發流程，為未來將訓練好的策略部署到實體 Microduck 機器人提供了可複製的技術路徑。

---