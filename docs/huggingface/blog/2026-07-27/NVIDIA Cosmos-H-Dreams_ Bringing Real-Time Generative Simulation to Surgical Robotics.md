# NVIDIA Cosmos-H-Dreams: Bringing Real-Time Generative Simulation to Surgical Robotics

- **來源**: Hugging Face Blog
- **發布日期**: 2026-07-27
- **原文連結**: https://huggingface.co/blog/nvidia/cosmos-h-dreams

## 核心主題
NVIDIA 推出 Cosmos-H-Dreams，將實時生成式模擬引入外科機器人領域，使外科手術模擬能即時互動，為政策評估與數據生成提供新工具。

## 關鍵重點
- **即時互動能力**：Cosmos-H-Dreams 是 Cosmos-H-Surgical-Simulator 的即時版本，可在單一 NVIDIA RTX PRO 6000 GPU 上運行，支援約 160 幀每秒的互動操作。
- **教師到學生訓練流程**：透過自強制蒸馏技術，將大型教師模型壓縮為輕量學生模型，解決長序列生成中的錯誤累積問題。
- **多平台支援**：已與 CMR Surgical 和 Cambridge Consultants 合作，整合至 Versius 外科控制器，並可擴展至其他外科機器人平台。
- **即時推論引擎**：透過 FlashDreams 加速庫，結合 KV Cache 串流、CUDA Graph 捕捉等優化技術，實現低延遲推論。
- **可擴展性**：提供完整指南讓使用者可自訓模型，適應特定外科機器人平台與數據集。

## 結論
Cosmos-H-Dreams 開拓了外科模擬的新前沿，為外科政策開發、數據生成與評估提供安全的研究平台。雖然不替代診斷系統或物理機器人控制器，但為未來閉環外科物理 AI 奠定基礎，可生成罕見失敗案例、支援強化學習，並加速新政策評估。

---