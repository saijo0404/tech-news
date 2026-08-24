# Maximizing AI Factory Performance per Watt with NVIDIA DSX MaxLPS

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-08-21
- **原文連結**: https://developer.nvidia.com/blog/maximizing-ai-factory-performance-per-watt-with-nvidia-dsx-maxlps/

## 核心主題
NVIDIA DSX MaxLPS 透過整合動態電力分配、先進的每瓦特效能優化技術以及 45°C 熱設計，在固定電力預算下最大化 AI 工廠吞吐量，重新找回因傳統靜態機架供電方案而遺棄的容量。

## 關鍵重點
- **動態電力軟體 (DPS)**：實現跨機架和 GPU 的細粒度、實時電力重新分配，利用遥測數據和策略驅動控制來維持最佳利用率，適應場級事件，避免手動重新配置。
- **驗證成果**：在 NVIDIA Vera Rubin NVL72 和 GB200 NVL72 系統上驗證，MaxLPS 減少每機架電力需求，可在相同設施包圍內增加高達 40% 的 GPU 容量，每瓦特效能提升 1.3-1.5 倍。
- **45°C 液冷設計**：透過暖水液冷降低冷卻過載，提高電力使用效率 (PUE)，將更多電力直接轉換為計算能力。

## 結論
MaxLPS 透過重新利用傳統靜態機架供電所遺棄的容量，顯著提高 AI 工廠的每瓦特效能和吞吐量，使數據中心不再以「能裝多少 GPU」為目標，而是以「每兆瓦能產生多少 AI 輸出」為關鍵指標。

---