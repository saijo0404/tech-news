# 5 Steps to Create SimReady Assets for Robotics with Frontier AI Models

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-10-08
- **原文連結**: https://developer.nvidia.com/blog/5-steps-to-create-simready-assets-for-robotics-with-frontier-ai-models/

## 核心主題
這篇文章介紹了如何使用 NVIDIA Omniverse 工具和 SimReady Foundation 規範，透過五個步驟將 CAD 資產轉換為適合機器人模擬的 OpenUSD 資產。

## 關鍵重點
- 五個步驟工作流程：從 STEP 檔案導入、視覺外觀匹配、物理屬性配置、SimReady 驗證，到最終的抓取放置任務
- 使用 Frontier AI 模型（如 GPT-6 Astra）協助每個步驟，減少手動準備工作
- 以 ABB YuMi 機器人為例，展示了雙臂和夾爪的完整工作流程
- 物理配置使用製造商數據表和公開 URDF 來定義關節軸、限制和質量屬性
- SimReady 驗證檢查單位、幾何形狀、材料、剛體、關節、驅動器和關節化以及運行時行為

## 結論
透過這些步驟，開發者可以確保機器人模型在模擬環境中正確運作，並通過 SimReady 驗證標準，從而提升機器人模擬的準確性和可靠性。
---