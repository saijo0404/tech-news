# Connecting Energy Use to Scientific Output with Science per Joule

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-11-18
- **原文連結**: https://developer.nvidia.com/blog/connecting-energy-use-to-scientific-output-with-science-per-joule/

## 核心主題
這篇文章探討了如何將能源消耗與科學輸出聯繫起來，通過「科學每瓩」(science per joule) 這一關鍵指標，評估 NVIDIA GB200 NVL72 與 HGX H100 在不同科學工作負載中的能源效率表現。

## 關鍵重點
- **科學每瓩指標**：將能源使用與科學輸出直接關聯，包括分子動力學（原子時間步每瓩）、氣候模擬（模擬天數每瓩）和 AI 生物學工作負載（預測和設計每瓩）。
- **GB200 NVL72 性能優勢**：在四個 LAMMPS 模擬中，GB200 NVL72 比 HGX H100 多 9-17% 的原子時間步每瓩，使用相同數量 GPU 的情況下。
- **系統整合效益**：在 ICON 氣候模擬中，GB200 NVL72 使用 40% 較少的 GPU（72 顆 vs 120 顆），達到 20% 更高的模擬天數每瓩，且時間至解決方案幾乎相同。
- **測量層級重要性**：系統級別測量（IT 設備直流電）比 GPU 單獨測量更能完整反映效率增益，因為非 GPU 組件在兩平台上功耗相似。
- **工作負載影響**：AI 推理工作負載（OpenFold3 和 RFD4-Proteina）顯示科學每瓩隨問題大小和工作負載行為變化顯著，單顆 B200 GPU 上可達 31-45 倍差異。

## 結論
NVIDIA 通過全棧創新（記憶體容量、NVLink 連接性、棧級集成和軟體電力管理）最大化科學每瓩。對於 HPC 中心，關鍵在於在固定電力預算下，將每瓩的支出轉化為有用的科學成果，而非僅關注 FLOPS 每秒或 PUE。

---