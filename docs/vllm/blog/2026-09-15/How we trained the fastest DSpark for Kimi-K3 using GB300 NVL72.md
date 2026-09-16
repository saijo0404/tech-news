# How we trained the fastest DSpark for Kimi-K3 using GB300 NVL72

- **來源**: vLLM Blog
- **發布日期**: 2026-09-15
- **原文連結**: https://vllm.ai/blog/2026-09-15-kimi-k3-dspark

## 核心主題
vLLM 團隊成功使用 Speculators 訓練庫，在 GB300 NVL72 硬體上訓練了 Kimi K3 的 DSpark 推測解碼模型，大幅提升推理速度與吞吐量。

## 關鍵重點
- **DSpark 演算法優勢**：結合平行推測與序列修正機制，比 DFlash 多接受 16-18% 序列，比 EAGLE-3 多 27-31%，單流互動性從 ~110 提升至 ~435 tok/s/user。
- **訓練架構創新**：使用 Mooncake 隱藏狀態傳輸系統，支援跨節點訓練，解決 2.8T 參數模型 VRAM 限制問題。
- **硬體與部署**：訓練於 Verda 提供的 GB300 NVL72 伺服器，支援 CUDA 13.4.0 及 Rubin 架構，可透過 Docker 容器快速部署。
- **性能表現**：在數學推理任務上達 6.42 tokens/驗證回合，長上下文提示下最高達 5.31 tokens/迭代，並能隨請求數量增加而擴展。

## 結論
vLLM 的 Speculators 訓練庫已驗證可支援大型模型（如 Kimi K3）的 DSpark 推測解碼，並與 vLLM 推理引擎完美整合，為開源社群提供易於訓練、包裝與部署的解決方案。

---