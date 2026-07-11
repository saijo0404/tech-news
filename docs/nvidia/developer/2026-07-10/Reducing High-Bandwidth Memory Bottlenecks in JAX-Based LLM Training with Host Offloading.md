# 降低 JAX 基於 LLM 訓練中的高頻寬記憶體瓶頸

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-07-10
- **原文連結**: https://developer.nvidia.com/blog/reducing-high-bandwidth-memory-bottlenecks-in-jax-based-llm-training-with-host-offloading/

## 核心主題
本文介紹了 NVIDIA 如何透過 JAX 框架中的「Host Offloading」技術，將部分激活值（activations）從 GPU 高頻寬記憶體（HBM）移至主機記憶體，以解決大型語言模型訓練時的記憶體瓶頸問題。

## 關鍵重點
- **技術原理**: Host Offloading 在正向傳播階段將選定的激活值移至主機記憶體，在反向傳播階段再流式傳回，替代昂貴的激活值重計算（activation rematerialization）。
- **硬體優勢**: 特別適合 NVIDIA Blackwell 平台，因其 CPU-GPU 間透過 NVLink-C2C 連接提供高達 900 GB/s 的頻寬（Vera Rubin 平台更達 1.8 TB/s）。
- **性能提升**: 在 DeepSeek-V3 671B 模型上，結合延遲隱藏調度器（LHS）與管道化傳輸，吞吐量提升達 57%，並能支援原本因記憶體限制無法運行的批次大小。
- **最佳實踐**: 需要透過 XLA 自訂排程旗標與專用複製串流來確保資料傳輸與運算/通訊工作負載有效重疊，並使用 NVIDIA Nsight Systems 等工具進行效能驗證。

## 結論
Host Offloading 是解決 GPU 記憶體限制、提升大型模型訓練可行性的關鍵技術，特別適合處理大型稀疏 MoE 模型。透過精心設計的重疊傳輸策略，可將原本受限的批次配置（如 micro batch 8, global batch 1024）從記憶體不足轉為可行，並大幅提升訓練吞吐量。

---

檔案已成功儲存至指定路徑。
