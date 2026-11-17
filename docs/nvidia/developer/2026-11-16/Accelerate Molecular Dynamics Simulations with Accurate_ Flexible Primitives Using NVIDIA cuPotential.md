# Accelerate Molecular Dynamics Simulations with Accurate, Flexible Primitives Using NVIDIA cuPotential

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-11-16
- **原文連結**: https://developer.nvidia.com/blog/accelerate-molecular-dynamics-simulations-with-accurate-flexible-primitives-using-nvidia-cupotential/

## 核心主題
NVIDIA cuPotential 是一個專注於分子動力學模擬的庫，透過模組化 C API 原語和 OpenMM 插件，優化長距離相互作用評估，提供 2-3 倍加速並保持高精度。

## 關鍵重點
- cuPotential 提供模組化 C API 原語，可加速分子動力學模擬中的長距離相互作用評估，特別是在週期邊界條件下的電靜學和色散相互作用。
- 透過 OpenMM 插件實現無縫整合，替換非鍵合力、朗之萬積分器和蒙特卡羅壓控器，使用者只需最小代碼變更即可獲得加速。
- 在 T4 到 RTX PRO 6000 Blackwell 等 GPU 架構上，24,000 至 400,000 原子系統可獲得 2-3 倍端到端加速。
- 與 D. E. Shaw Research 和 Flatiron Institute 合作開發的新 C2 連續分割和擴散函數，在更低網格解析度和截斷距離下達到與標準 Ewald 和 u-series 方法相同的精度。
- 能量漂移測量顯示 cuPotential 將漂移減少數百倍，散佈能量精度提升數千倍，同時保持相當的力誤差。

## 結論
cuPotential 為生物分子模擬提供高效且準確的加速解決方案，特別適合需要高精度長距離相互作用評估的應用場景。開發者可以透過簡單的插件整合方式，在不影響模擬結果精度的前提下，顯著提升模擬效率。

---

更多資源：[NVIDIA/cuPotential GitHub 倉庫](https://github.com/NVIDIA/cuPotential)
