# Run GPU-Powered Black Hole Interferometry with NVIDIA cuPhoton

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-11-13
- **原文連結**: https://developer.nvidia.com/blog/run-gpu-powered-black-hole-interferometry-with-nvidia-cuphoton/

## 核心主題
本文介紹 NVIDIA cuPhoton.xBeam 如何加速射電干涉儀相關計算，用於事件視界望遠鏡（EHT）的黑洞成像研究，透過 GPU 處理海量天文數據。

## 關鍵重點
- **460 倍加速**：在 NVIDIA Vera Rubin NVL72 系統（64 GPU + GPUDirect Storage）上，xBeam 將 10TB 數據集相關處理從 8.89 小時縮短至 70 秒。
- **五步驟處理流程**：xBeam 執行 ingest（讀取 VDIF）、delay/fringe correction（延遲與相位校正）、channelization（頻道化）、cross-multiply（交叉相乘）及 write visibilities（寫入可見度）。
- **彈性擴展架構**：支援單一節點多 GPU（--devices）與跨節點分片（--shard-count/--shard-index），透過 merge-shards 整合部分結果。
- **AI 自動化整合**：AI 代理可解析 VDIF 元資料、生成 JSON 工作指令、啟動 xBeam 相關並監控執行。

## 結論
cuPhoton.xBeam 為天文學研究提供強大的 GPU 加速工具，大幅降低黑洞成像數據處理門檻，使下一代事件視界望遠鏡（ngEHT）能更高效地處理海量射電數據。

---