# From Materials Simulation to Experimental Astronomy: New NVIDIA AI Software Unlocks Scientific Discoveries

- **來源**: NVIDIA Blogs
- **發布日期**: 2026-06-22
- **原文連結**: https://blogs.nvidia.com/blog/ai-for-science-software-cuda/

## 核心主題
NVIDIA 於 ISC 2026 推出多款 AI 科學軟體——DAQIRI、ALCHEMI NIM 微服務與 cuPhoton 參考程式碼，將過去需數小時至數天的 CPU 運算轉為即時 GPU 加速管線，加速從化學、材料探索到暗物質搜尋的科學研究。

## 關鍵重點
- **cuPhoton：天文數據處理速度提升近 15,000 倍**：cuPhoton 為專為多維天文與觀測數據設計的參考程式碼，可載入、處理、分析並可視化 PB 等級資料。在 Rubin Observatory 的 LSST 相機數據測試中，資料載入與讀取速度提升 14,900 倍，使用 32 顆 Grace Blackwell superchips 的訊號處理與分析速度提升 8,400 倍，讓全球最大數位相機的觀測數據能更快轉化為科學洞察。
- **DAQIRI 與 ALCHEMI：即時儀表串流與材料模擬加速器**：DAQIRI 為高性能網路程式庫，將高速偵測器與感測器的資料即時串流至 NVIDIA 軟體生態系，避免舊有硬體系統因資料產出速率過高而遺失數據。CERN 的 A-GHOST 專案利用 DAQIRI 對 ATLAS 實驗被捨棄的 99% 碰撞數據進行即時 AI 分析，捕捉原本會遺失的潛在interesting訊號。ALCHEMI 則包含批次幾何弛豫（BGR）與批次分子動力學（BMD）微服務，讓研究者能一次模擬數百萬分子與材料，並預計推出 VASP 微服務（透過 MPS 單一 GPU 多運算實現 3 倍幾何最佳化加速）。
- **Lila Sciences 展示 ALCHEMI 的產業應用**：Lila Sciences 使用 ALCHEMI BGR 微服務將高通量材料篩選加速 50 倍，並使用 VASP 微服務加速磁性屬性計算 30%。TensorNet 專門核心在 AI 代理模型訓練與推論上提供 6 倍加速並減少 3 倍記憶體使用，將原本需數週的模擬縮短至數天。Lila Sciences 結合 Megatron-LM、Nemotron、BioNeMo、Triton 與 Omniverse 等完整 NVIDIA 堆疊，建構自主實驗室與科學超級智慧平台。

## 結論
NVIDIA DAQIRI、ALCHEMI 與 cuPhoton 代表了「從實驗室到望遠鏡」的端到端加速解決方案——將物理科學數據生成、即時儀表串流與多維天文資料處理整合在同一個 CUDA-X 生態系中。這些工具已分別開放於 GitHub、NGC 與 PyPI 下載，讓全球科學家能以個人在過去無法企及的規模，加速材料發現、能源催化劑開發與天體物理研究。

---
