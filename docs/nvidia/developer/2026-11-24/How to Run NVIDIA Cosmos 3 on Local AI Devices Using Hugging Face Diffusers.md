# How to Run NVIDIA Cosmos 3 on Local AI Devices Using Hugging Face Diffusers

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-11-24
- **原文連結**: https://developer.nvidia.com/blog/how-to-run-nvidia-cosmos-3-on-local-ai-devices-using-hugging-face-diffusers/

## 核心主題
本文介紹如何在本地 AI 設備上運行 NVIDIA Cosmos 3 Nano，使用 Hugging Face Diffusers 實現記憶體優化和本地部署，支援低至 12 GB VRAM 的設備。

## 關鍵重點
- **7 種生成模式**：支援文字到影片 (T2V)、圖片到影片 (I2V)、影片到影片 (V2V)、聲音生成、動作生成、控制引導生成及多模態組合。
- **記憶體優化方案**：透過 Cosmos-Framework 與 Hugging Face Diffusers 實現，將模型權重儲存於系統 RAM，僅在需要時轉移至 GPU，支援 12 GB VRAM 設備。
- **FP8 精度優勢**：FP8 檢查點推理速度比 BF16 快約 15-20%，峰值記憶體使用量略低，可大幅降低硬體門檻。
- **GPU 性能測試**：測試涵蓋 RTX 5070/5080/4090/5090，RTX 5070 在 720p 下生成 T2V 需約 2,625 秒，峰值記憶體 9.94 GiB。
- **解析度影響**：1280×720 解析度生成時間最長（RTX 5070 BF16 約 43.75 分鐘），432×240 最快（約 3.46 分鐘）。
- **部署步驟**：克隆 cosmos-framework、安裝 diffusers-cpu-offloading、使用 StreamingConfig 配置設備、透過 build_pipeline 載入模型。

## 結論
透過 NVIDIA Cosmos 3 Nano 和本地部署方案，即使只有 12 GB VRAM 的設備也能運行高階 AI 生成模型，大幅降低硬體門檻，適合開發者和小型團隊快速原型開發。建議從 Hugging Face 下載檢查點，並參考 Cosmos-Framework 範例程式碼進行部署。

---