# ReplaySSM: Rethinking State Storage for Faster Hybrid-Model Decoding

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-10-12
- **原文連結**: https://developer.nvidia.com/blog/replayssm-rethinking-state-storage-for-faster-hybrid-model-decoding/

## 核心主題
NVIDIA 與普林大學 Dao AI Lab 合作開發的 ReplaySSM 技術，透過將 SSM 狀態表示為檢查點加最近輸入緩衝區，重新設計混合模型中的狀態儲存方式，顯著提升解碼速度並降低記憶體流量。

## 關鍵重點
- **降低記憶體流量**：狀態讀寫頻率減少約一半，在 batch size 256 時解碼速度提升 1.46x~1.80x
- **簡化推測式解碼**：透過緩衝區管理取代狀態快照，120B 級模型推測吞吐量提升 1.85x~2.10x
- **降低量化錯誤**：檢查點使用高精度，讀取使用低精度，四分之三模型在 GPQA-Diamond 測試中誤差控制在 2% 以內

## 結論
ReplaySSM 已整合至多個開源推理框架（TensorRT-LLM、vLLM、FlashInfer）並投入生產部署（GLM-5.3-Flash、Kimi-K3），為混合模型推理帶來顯著性能提升。

---

## 技術細節補充
- **核心概念**：將 SSM (State-Space Model) 狀態表示為「檢查點 + 最近輸入緩衝區」，將輸出計算與狀態更新分離。
- **應用現況**：已整合至 NVIDIA TensorRT-LLM、vLLM 和 FlashInfer，並已在 GLM-5.3-Flash 與 Kimi-K3 等模型中生產部署。
- **精度優化研究**：
  - FP16 隨機捨入 (SR) 的迴歸檢查點能緊跟 FP32
  - 共享 NVFP4 檢查點導致 3-31% 準確性損失
  - 使用 FP16/FP8 迴歸可恢復大部分準確性
- **框架整合**：ReplaySSM 已整合至多個開源推理框架，包括 TensorRT-LLM、vLLM、SGLang 和 FlashInfer。
- **作者背景**：來自 Princeton University Dao AI Lab 和 NVIDIA 團隊，專注於 LLM 推理效率與混合模型優化。
