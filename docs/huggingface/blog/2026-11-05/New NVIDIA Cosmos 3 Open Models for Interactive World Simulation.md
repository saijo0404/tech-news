# New NVIDIA Cosmos 3 Open Models for Interactive World Simulation

- **來源**: Hugging Face
- **發布日期**: 2026-11-05
- **原文連結**: https://huggingface.co/blog/nvidia/cosmos-interactive-world-simulation

## 核心主題
NVIDIA 推出了四款新的開源模型，用於生成互動式世界模擬和多感器多視角駕駛場景。

## 關鍵重點
- **Cosmos3-Nano-Transfer-Auto**：生成多視角駕駛數據，包含多變化的天氣、光照和時間條件，支援最多 11 個相機視角及 RGB-LiDAR 聯合生成。
- **Cosmos3-Nano-Sim-Auto**：流式同步相機和 LiDAR 觀察，支援快速串流和長時互動模擬，透過因果訓練和壓縮技術實現高效生成。
- **Cosmos3-Nano-Sim-Transfer**：將模擬器控制器和文字提示轉換為照片級視頻，支援深度、分割、邊緣和模糊等空間控制。
- **Cosmos3-Nano-Sim-Bimanual**：預測來自機器人雙臂動作或相機操作的視頻，支援 YAM 和 AgiBot 等實體的互動式雙臂模擬。

## 結論
這些模型均為 Cosmos 3 Nano 的後訓練版本，擁有 16B 可訓練參數，採用 OpenMDW1.1 許可，允許商業和非商業使用。它們為研究人員和開發者提供了共享的起始點，可透過後訓練配方適應自己的數據集，並支援從數據生成到模型適配的完整開發流程。

---