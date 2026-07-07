# LeRobot v0.6.0 Release

- **來源**: Hugging Face Blog
- **發布日期**: 2026-07-07
- **原文連結**: https://huggingface.co/blog/lerobot-release-v060

## 核心主題
LeRobot v0.6.0 帶來了世界模型政策、新 VLA 模型、獎勵模型、數據集改進、評估工具以及訓練與部署的全面提升。

## 關鍵重點
- **世界模型政策**: 推出 VLA-JEPA（訓練時預測未來，推理時零額外成本）、LingBot-VA（自回歸式視頻行動模型）和 FastWAM（整合視頻生成與行動專家）
- **新 VLAs**: 新增 GR00T N1.7（NVIDIA 最新開放源碼模型）、MolmoAct2（支援 SO-100/100 機器人）、EO-1（Qwen2.5-VL-3B 背骨）、Multitask DiT 和 EVO1（0.77B 參數小型政策）
- **獎勵模型**: 推出 Robometer（通用目的獎勵模型，4B 參數）和 TOPReward（完全零樣本獎勵模型）
- **數據集改進**: 支援深度感測（Intel RealSense）、自動語言標註（VLM 自動標註）、自訂視頻編碼（支援 NVENC 等硬體編碼器），數據載入速度提升 2 倍
- **評估工具**: 新增六項新基準測試（LIBERO-plus、RoboTwin 2.0、RoboCasa365、RoboCerebra、RoboMME、VLABench），lerobot-eval CLI 統一評估，評估速度提升 2 倍
- **訓練與部署**: 新增 lerobot-rollout CLI 專用部署工具，支援 FSDP（訓練大於單卡 GPU 的模型）、雲端訓練（HF Jobs）和 DAgger 式人類迴圈修正
- **DaGger 策略優化**: 支援即時干預與無震動接管，自動標記修正數據集供後續微調
- **FSDP 訓練支援**: 透過 Accelerate 支援全量分片數據並行，可跨多 GPU 訓練並恢復檢查點
- **雲端訓練 (HF Jobs)**: 新增單一旗標即可在雲端訓練，支援 T4 至 8x H200 計算資源，按量計費
- **安裝優化**: pip 安裝更輕量，依賴減少約 40%，支援功能範圍分組安裝
- **PyTorch 升級**: 支援 PyTorch 2.7–2.11，預設鎖定 CUDA 12.8 輪
- **視覺化工具**: 整合 Foxglove 進行遠端遙控與數據集回放
- **LeLab 瀏覽器介面**: 無需 CLI 即可完成完整工作流，支援 SO-ARM101
- **VR 遙控**: 透過 Isaac Teleop 支援 VR 控制器遙控 SO-101
- **硬體指南**: 提供從 RTX 4090 到 4x H100 的 VRAM 包絡與訓練時間參考
- **社區貢獻**: 包含數百個錯誤修復與品質生活升級

## 結論
LeRobot v0.6.0 是重大更新，帶來了世界模型、新 VLA 模型、獎勵模型、數據集改進、評估工具和訓練部署的全面提升，並優化了安裝和雲端訓練功能，為機器人學習生態系帶來更多選擇與效率。

---

此摘要已儲存至指定檔案路徑。
