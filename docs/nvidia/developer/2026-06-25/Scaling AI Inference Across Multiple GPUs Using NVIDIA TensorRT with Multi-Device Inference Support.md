---
# Scaling AI Inference Across Multiple GPUs Using NVIDIA TensorRT with Multi-Device Inference Support

- **來源**: NVIDIA Technical Blog
- **發布日期**: 2026-06-25
- **原文連結**: https://developer.nvidia.com/blog/scaling-ai-inference-across-multiple-gpus-using-nvidia-tensorrt-with-multi-device-inference-support/

## 核心主題
NVIDIA TensorRT 11.0 導入原生多裝置推論功能，結合 NCCL 分散式通訊庫與上下文並行策略，讓生成式 AI 模型（如影像與影片生成）能無縫擴展至多張 GPU，突破單一裝置的記憶體與運力限制。

## 關鍵重點
- **NCCL 整合與全集合操作支援**：TensorRT 11.0 直接整合 NVIDIA NCCL，自動選擇最佳傳輸協定（NVLink、NVSwitch、PCIe、InfiniBand），並支援 AllReduce、Broadcast、AllGather、AlltoAll 等全套分散式集合操作，為多 GPU 推論提供高效能通訊基礎。
- **三種上下文並行策略比較**：（1）AllGather KV：各 GPU 交換 K/V 分片後計算全域注意力，每層增加一次集合操作但有效縮小本地矩陣乘法；（2）Ring Attention：透過環狀拓撲重疊通訊與運算，並使用 online softmax 降低 K/V 記憶體佔用；（3）DeepSpeed Ulysses：將 Q/K/V 分片後以 all-to-all 通訊確保每個 GPU 獲得完整序列但僅處理不重疊的注意力頭，實現並行注意力計算。
- **效能基準測試結果與專業團隊**：在 NVIDIA Cosmos 3（影片生成）與 FLUX.1（影像生成）的 8 GPU 測試中，DeepSpeed Ulysses 在極長上下文（數萬 tokens）場景下 consistently 達成最低延遲，Ring Attention 在 4 GPU 上亦展現良好擴展性。本文由五位涵蓋編譯器、執行期架構、分散式通訊與 GPU Kernel 開發的 TensorRT 工程師共同撰寫，技術根植於 NCCL 與多項上下文並行創新研究。

## 結論
TensorRT 11.0 的多裝置推論功能為生成式 AI 的生產部署提供了完整的解決方案——從 PyTorch 模型經 Torch-TensorRT 轉換為 TensorRT 引擎，再部署至 C++ 推論應用，全程保留 kernel 融合、記憶體最佳化與量化等生產級優化。對於上下文長度達數萬 tokens 的影片與影像生成管線，DeepSpeed Ulysses 策略在多 GPU 擴展上表現最為突出，而 Ring Attention 則是中等 GPU 數量下的高效能替代方案。

---
