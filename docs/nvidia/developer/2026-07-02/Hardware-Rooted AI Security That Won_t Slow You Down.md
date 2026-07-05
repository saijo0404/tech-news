# Hardware-Rooted AI Security That Won't Slow You Down

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-07-02
- **原文連結**: https://developer.nvidia.com/blog/hardware-rooted-ai-security-that-wont-slow-you-down/

## 核心主題
NVIDIA 介紹其 **Confidential Computing（CC）硬體級机密計算**方案——在 Blackwell GPU 上內建加密與遠端證明機制，在保護企業數據、模型權重與推理過程的同時，維持高達 **98% 的原始推理效能**。

## 關鍵重點
- **硬體級安全信任鏈**：NVIDIA Blackwell GPU（包括 RTX PRO 6000、HGX B200、HGX B300）在晶片製造時即內建永久性的私密簽署金鑰，永不暴露於軟體、韌體或主機系統。推理前執行**遠端證明**——NVIDIA 遠端證明服務（NRAS）驗證 GPU 硬體報告與 CPU TEE（AMD SEV-SNP 或 Intel TDX）測量值，確認系統處於未修改狀態後才部署解密密鑰。證明僅在啟動時執行一次，不增加個別推理請求的延遲。
- **CC 效能優化三大創新**：①**CC-safe autotuner**——FlashInfer 將事件計時器替換為 GPU 全域計時器，確保 autotuner 在 CC 模式下仍能準確比較核心效能。②**非同步 D2H 複製工作執行緒**——SGLang 將每個步驟的 token 讀回移出排程器的關鍵路徑，恢復計算與複製重疊。③**分段 CUDA Graph 支援**——SGLang 為 prefill 和混合批次加入 CUDA Graph 重播，降低被 CC 放大的核心啟動開銷。
- **基準測試結果（Qwen3.5-397B-A17B-FP8 / HGX B300）**：在各種併發量（4-256）、輸入/輸出 token 長度（1024/1024 與 8192/1024）下，CC 開啟時的吞吐量衰減僅 **1%-7.5%**、中位 TPOT 衰減 **0.9%-8.1%**。大併發量（32-128）且長輸入序列（8192）時表現最佳（吞吐量衰減僅 1%-3.5%），小併發量短序列時因核心啟動開銷影響較大。整體證明 CC 可在生產環境中安全部署而不顯著犧牲效能。

## 結論
NVIDIA Confidential Computing 為企業 AI 推理提供了一個**安全性與效能兼備**的方案——透過 Blackwell GPU 的硬體級信任鏈、遠端證明機制，以及與 FlashInfer 和 SGLang 等推理框架的深度優化合作，CC 能在保護數據隱私、模型智慧財產權和合規性（GDPR、HIPAA）的同時，維持高達 98% 的推理效能。對於需要在生產環境中部署 AI 但受安全法規限制的企业而言，CC 提供了一個可實際落地的机密計算路徑。

---
